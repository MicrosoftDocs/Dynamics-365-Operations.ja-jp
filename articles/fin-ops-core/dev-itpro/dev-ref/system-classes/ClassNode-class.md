---
title: ClassNode クラス
description: このトピックでは、ClassNode クラスについて説明します。
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
ms.openlocfilehash: 83cda89cf097ef5e78884aa311a9cfec0cfd3ab4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502712"
---
# <a name="class-classnode"></a><span data-ttu-id="e8714-103">クラス ClassNode</span><span class="sxs-lookup"><span data-stu-id="e8714-103">Class ClassNode</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class ClassNode extends TreeNode
```

<span data-ttu-id="e8714-104">ClassNode クラスは、アプリケーション オブジェクト ツリー (AOT) のクラスを表す TreeNode クラスの特殊な形式です。</span><span class="sxs-lookup"><span data-stu-id="e8714-104">The ClassNode class is a specialization of the TreeNode class that represents a class in the Application Object Tree (AOT).</span></span>

## <a name="remarks"></a><span data-ttu-id="e8714-105">備考</span><span class="sxs-lookup"><span data-stu-id="e8714-105">Remarks</span></span>

<span data-ttu-id="e8714-106">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="e8714-106">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="e8714-107">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e8714-107">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="e8714-108">例</span><span class="sxs-lookup"><span data-stu-id="e8714-108">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="e8714-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="e8714-109">Methods</span></span>

| <span data-ttu-id="e8714-110">方法</span><span class="sxs-lookup"><span data-stu-id="e8714-110">Method</span></span>                                            | <span data-ttu-id="e8714-111">説明</span><span class="sxs-lookup"><span data-stu-id="e8714-111">Description</span></span>                                                                                                                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8714-112">public TreeNode AOToverrideMethod(str methodName)</span><span class="sxs-lookup"><span data-stu-id="e8714-112">public TreeNode AOToverrideMethod(str methodName)</span></span> |                                                                                                                                               |
| <span data-ttu-id="e8714-113">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e8714-113">public str changedBy(\[str value\])</span></span>               | <span data-ttu-id="e8714-114">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8714-114">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="e8714-115">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="e8714-115">public Date changedDate(\[Date value\])</span></span>           | <span data-ttu-id="e8714-116">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8714-116">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="e8714-117">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e8714-117">public str changedTime(\[str value\])</span></span>             | <span data-ttu-id="e8714-118">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8714-118">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="e8714-119">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e8714-119">public str createdBy(\[str value\])</span></span>               | <span data-ttu-id="e8714-120">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8714-120">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="e8714-121">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="e8714-121">public Date creationDate(\[Date value\])</span></span>          | <span data-ttu-id="e8714-122">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8714-122">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="e8714-123">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e8714-123">public str creationTime(\[str value\])</span></span>            |                                                                                                                                               |
| <span data-ttu-id="e8714-124">public str extends(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e8714-124">public str extends(\[str value\])</span></span>                 |                                                                                                                                               |
| <span data-ttu-id="e8714-125">public int iD(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e8714-125">public int iD(\[int value\])</span></span>                      |                                                                                                                                               |
| <span data-ttu-id="e8714-126">public boolean isDetached()</span><span class="sxs-lookup"><span data-stu-id="e8714-126">public boolean isDetached()</span></span>                       |                                                                                                                                               |
| <span data-ttu-id="e8714-127">public int legacyId(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e8714-127">public int legacyId(\[int value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="e8714-128">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e8714-128">public str name(\[str value\])</span></span>                    | <span data-ttu-id="e8714-129">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8714-129">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="e8714-130">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="e8714-130">public Guid origin(\[Guid value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="e8714-131">public int runOn(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="e8714-131">public int runOn(\[int value\])</span></span>                   |                                                                                                                                               |
| <span data-ttu-id="e8714-132">public void AOTedit(\[int Line\], \[int Column\])</span><span class="sxs-lookup"><span data-stu-id="e8714-132">public void AOTedit(\[int Line\], \[int Column\])</span></span> | <span data-ttu-id="e8714-133">クラスを開き、エディターで変更することもできるようにします。</span><span class="sxs-lookup"><span data-stu-id="e8714-133">Opens the class so that it can be modified in the editor.</span></span>                                                                                     |

## <a name="method-aotoverridemethod"></a><span data-ttu-id="e8714-134">メソッド AOToverrideMethod</span><span class="sxs-lookup"><span data-stu-id="e8714-134">Method AOToverrideMethod</span></span>

```xpp
public TreeNode AOToverrideMethod(str methodName)
```

### <a name="parameters---aotoverridemethod"></a><span data-ttu-id="e8714-135">パラメーター - AOToverrideMethod</span><span class="sxs-lookup"><span data-stu-id="e8714-135">Parameters - AOToverrideMethod</span></span>

<span data-ttu-id="e8714-136">methodName</span><span class="sxs-lookup"><span data-stu-id="e8714-136">methodName</span></span>  

### <a name="return-value---aotoverridemethod"></a><span data-ttu-id="e8714-137">戻り値 - AOToverrideMethod</span><span class="sxs-lookup"><span data-stu-id="e8714-137">Return Value - AOToverrideMethod</span></span>

## <a name="method-changedby"></a><span data-ttu-id="e8714-138">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="e8714-138">Method changedBy</span></span>

<span data-ttu-id="e8714-139">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8714-139">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="e8714-140">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="e8714-140">Parameters - changedBy</span></span>

<span data-ttu-id="e8714-141">値</span><span class="sxs-lookup"><span data-stu-id="e8714-141">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="e8714-142">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="e8714-142">Return Value - changedBy</span></span>

<span data-ttu-id="e8714-143">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="e8714-143">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="e8714-144">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="e8714-144">Method changedDate</span></span>

<span data-ttu-id="e8714-145">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8714-145">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="e8714-146">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="e8714-146">Parameters - changedDate</span></span>

<span data-ttu-id="e8714-147">値</span><span class="sxs-lookup"><span data-stu-id="e8714-147">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="e8714-148">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="e8714-148">Return Value - changedDate</span></span>

<span data-ttu-id="e8714-149">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="e8714-149">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="e8714-150">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="e8714-150">Method changedTime</span></span>

<span data-ttu-id="e8714-151">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8714-151">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="e8714-152">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="e8714-152">Parameters - changedTime</span></span>

<span data-ttu-id="e8714-153">値</span><span class="sxs-lookup"><span data-stu-id="e8714-153">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="e8714-154">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="e8714-154">Return Value - changedTime</span></span>

<span data-ttu-id="e8714-155">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="e8714-155">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="e8714-156">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="e8714-156">Method createdBy</span></span>

<span data-ttu-id="e8714-157">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8714-157">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="e8714-158">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="e8714-158">Parameters - createdBy</span></span>

<span data-ttu-id="e8714-159">値</span><span class="sxs-lookup"><span data-stu-id="e8714-159">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="e8714-160">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="e8714-160">Return Value - createdBy</span></span>

<span data-ttu-id="e8714-161">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="e8714-161">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="e8714-162">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="e8714-162">Method creationDate</span></span>

<span data-ttu-id="e8714-163">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8714-163">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="e8714-164">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="e8714-164">Parameters - creationDate</span></span>

<span data-ttu-id="e8714-165">値</span><span class="sxs-lookup"><span data-stu-id="e8714-165">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="e8714-166">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="e8714-166">Return Value - creationDate</span></span>

<span data-ttu-id="e8714-167">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="e8714-167">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="e8714-168">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="e8714-168">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="e8714-169">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="e8714-169">Parameters - creationTime</span></span>

<span data-ttu-id="e8714-170">値</span><span class="sxs-lookup"><span data-stu-id="e8714-170">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="e8714-171">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="e8714-171">Return Value - creationTime</span></span>

## <a name="method-extends"></a><span data-ttu-id="e8714-172">メソッド extends</span><span class="sxs-lookup"><span data-stu-id="e8714-172">Method extends</span></span>

```xpp
public str extends([str value])
```

### <a name="parameters---extends"></a><span data-ttu-id="e8714-173">パラメーター - extends</span><span class="sxs-lookup"><span data-stu-id="e8714-173">Parameters - extends</span></span>

<span data-ttu-id="e8714-174">値</span><span class="sxs-lookup"><span data-stu-id="e8714-174">value</span></span>  

### <a name="return-value---extends"></a><span data-ttu-id="e8714-175">戻り値 - extends</span><span class="sxs-lookup"><span data-stu-id="e8714-175">Return Value - extends</span></span>

## <a name="method-id"></a><span data-ttu-id="e8714-176">メソッド iD</span><span class="sxs-lookup"><span data-stu-id="e8714-176">Method iD</span></span>

```xpp
public int iD([int value])
```

### <a name="parameters---id"></a><span data-ttu-id="e8714-177">パラメーター - iD</span><span class="sxs-lookup"><span data-stu-id="e8714-177">Parameters - iD</span></span>

<span data-ttu-id="e8714-178">値</span><span class="sxs-lookup"><span data-stu-id="e8714-178">value</span></span>  

### <a name="return-value---id"></a><span data-ttu-id="e8714-179">戻り値 - iD</span><span class="sxs-lookup"><span data-stu-id="e8714-179">Return Value - iD</span></span>

## <a name="method-isdetached"></a><span data-ttu-id="e8714-180">メソッド isDetached</span><span class="sxs-lookup"><span data-stu-id="e8714-180">Method isDetached</span></span>

```xpp
public boolean isDetached()
```

### <a name="return-value---isdetached"></a><span data-ttu-id="e8714-181">戻り値 - isDetached</span><span class="sxs-lookup"><span data-stu-id="e8714-181">Return Value - isDetached</span></span>

## <a name="method-legacyid"></a><span data-ttu-id="e8714-182">メソッド legacyId</span><span class="sxs-lookup"><span data-stu-id="e8714-182">Method legacyId</span></span>

```xpp
public int legacyId([int value])
```

### <a name="parameters---legacyid"></a><span data-ttu-id="e8714-183">パラメーター - legacyId</span><span class="sxs-lookup"><span data-stu-id="e8714-183">Parameters - legacyId</span></span>

<span data-ttu-id="e8714-184">値</span><span class="sxs-lookup"><span data-stu-id="e8714-184">value</span></span>  

### <a name="return-value---legacyid"></a><span data-ttu-id="e8714-185">戻り値 - legacyId</span><span class="sxs-lookup"><span data-stu-id="e8714-185">Return Value - legacyId</span></span>

## <a name="method-name"></a><span data-ttu-id="e8714-186">メソッド名</span><span class="sxs-lookup"><span data-stu-id="e8714-186">Method name</span></span>

<span data-ttu-id="e8714-187">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8714-187">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="e8714-188">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="e8714-188">Parameters - name</span></span>

<span data-ttu-id="e8714-189">値</span><span class="sxs-lookup"><span data-stu-id="e8714-189">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="e8714-190">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="e8714-190">Return Value - name</span></span>

<span data-ttu-id="e8714-191">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="e8714-191">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="e8714-192">備考 - name</span><span class="sxs-lookup"><span data-stu-id="e8714-192">Remarks - name</span></span>

<span data-ttu-id="e8714-193">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8714-193">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="e8714-194">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="e8714-194">Begins with a letter.</span></span>
-   <span data-ttu-id="e8714-195">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="e8714-195">Does not exceed 250 characters.</span></span>
-   <span data-ttu-id="e8714-196">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="e8714-196">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="e8714-197">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="e8714-197">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="e8714-198">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="e8714-198">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, classes, and so on.</span></span>

## <a name="method-origin"></a><span data-ttu-id="e8714-199">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="e8714-199">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="e8714-200">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="e8714-200">Parameters - origin</span></span>

<span data-ttu-id="e8714-201">値</span><span class="sxs-lookup"><span data-stu-id="e8714-201">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="e8714-202">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="e8714-202">Return Value - origin</span></span>

## <a name="method-runon"></a><span data-ttu-id="e8714-203">メソッド runOn</span><span class="sxs-lookup"><span data-stu-id="e8714-203">Method runOn</span></span>

```xpp
public int runOn([int value])
```

### <a name="parameters---runon"></a><span data-ttu-id="e8714-204">パラメーター - runOn</span><span class="sxs-lookup"><span data-stu-id="e8714-204">Parameters - runOn</span></span>

<span data-ttu-id="e8714-205">値</span><span class="sxs-lookup"><span data-stu-id="e8714-205">value</span></span>  

### <a name="return-value---runon"></a><span data-ttu-id="e8714-206">戻り値 - runOn</span><span class="sxs-lookup"><span data-stu-id="e8714-206">Return Value - runOn</span></span>

## <a name="method-aotedit"></a><span data-ttu-id="e8714-207">メソッド AOTedit</span><span class="sxs-lookup"><span data-stu-id="e8714-207">Method AOTedit</span></span>

<span data-ttu-id="e8714-208">クラスを開き、エディターで変更することもできるようにします。</span><span class="sxs-lookup"><span data-stu-id="e8714-208">Opens the class so that it can be modified in the editor.</span></span>

```xpp
public void AOTedit([int Line], [int Column])
```

### <a name="parameters---aotedit"></a><span data-ttu-id="e8714-209">パラメーター - AOTedit</span><span class="sxs-lookup"><span data-stu-id="e8714-209">Parameters - AOTedit</span></span>

<span data-ttu-id="e8714-210">折れ線</span><span class="sxs-lookup"><span data-stu-id="e8714-210">Line</span></span>  
<span data-ttu-id="e8714-211">無視される値、オプション。</span><span class="sxs-lookup"><span data-stu-id="e8714-211">A value that is ignored; optional.</span></span>

<!-- -->

<span data-ttu-id="e8714-212">円柱</span><span class="sxs-lookup"><span data-stu-id="e8714-212">Column</span></span>  
<span data-ttu-id="e8714-213">無視される値、オプション。</span><span class="sxs-lookup"><span data-stu-id="e8714-213">A value that is ignored; optional.</span></span>

### <a name="remarks---aotedit"></a><span data-ttu-id="e8714-214">備考 - AOTedit</span><span class="sxs-lookup"><span data-stu-id="e8714-214">Remarks - AOTedit</span></span>

<span data-ttu-id="e8714-215">すべてのメソッドはエディターに読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="e8714-215">All methods are loaded into the editor.</span></span> <span data-ttu-id="e8714-216">引数は、下位互換性のためにのみ署名に含まれているため、無視されます。</span><span class="sxs-lookup"><span data-stu-id="e8714-216">The arguments are included in the signature for backward compatibility only; they are ignored.</span></span>

### <a name="examples---aotedit"></a><span data-ttu-id="e8714-217">例 - AOTedit</span><span class="sxs-lookup"><span data-stu-id="e8714-217">Examples - AOTedit</span></span>

```xpp
static void example() 
{ 
    ClassNode classNode; 
```

```xpp
    classNode = infolog.findNode('\Classes\SysClassWizard'); 
    classNode.AOTedit(); 
}
```

