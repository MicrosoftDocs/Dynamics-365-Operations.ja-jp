---
title: CueGroup クラス
description: このトピックでは、CueGroup クラスについて説明します。
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
ms.openlocfilehash: e5fe874c3ffc0961debf3f4163f49d26f47141eb
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502700"
---
# <a name="class-cuegroup"></a><span data-ttu-id="cbd0f-103">クラス CueGroup</span><span class="sxs-lookup"><span data-stu-id="cbd0f-103">Class CueGroup</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class CueGroup extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="cbd0f-104">備考</span><span class="sxs-lookup"><span data-stu-id="cbd0f-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="cbd0f-105">例</span><span class="sxs-lookup"><span data-stu-id="cbd0f-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="cbd0f-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="cbd0f-106">Methods</span></span>

| <span data-ttu-id="cbd0f-107">方法</span><span class="sxs-lookup"><span data-stu-id="cbd0f-107">Method</span></span>                                   | <span data-ttu-id="cbd0f-108">説明</span><span class="sxs-lookup"><span data-stu-id="cbd0f-108">Description</span></span>                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd0f-109">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cbd0f-109">public str changedBy(\[str value\])</span></span>      | <span data-ttu-id="cbd0f-110">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-110">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="cbd0f-111">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="cbd0f-111">public Date changedDate(\[Date value\])</span></span>  | <span data-ttu-id="cbd0f-112">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-112">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="cbd0f-113">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cbd0f-113">public str changedTime(\[str value\])</span></span>    | <span data-ttu-id="cbd0f-114">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-114">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="cbd0f-115">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cbd0f-115">public str createdBy(\[str value\])</span></span>      | <span data-ttu-id="cbd0f-116">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-116">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="cbd0f-117">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="cbd0f-117">public Date creationDate(\[Date value\])</span></span> | <span data-ttu-id="cbd0f-118">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-118">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="cbd0f-119">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cbd0f-119">public str creationTime(\[str value\])</span></span>   |                                                                                                                                               |
| <span data-ttu-id="cbd0f-120">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cbd0f-120">public str label(\[str value\])</span></span>          | <span data-ttu-id="cbd0f-121">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-121">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="cbd0f-122">public str LabelId()</span><span class="sxs-lookup"><span data-stu-id="cbd0f-122">public str LabelId()</span></span>                     |                                                                                                                                               |
| <span data-ttu-id="cbd0f-123">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="cbd0f-123">public str name(\[str value\])</span></span>           | <span data-ttu-id="cbd0f-124">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-124">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="cbd0f-125">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="cbd0f-125">public Guid origin(\[Guid value\])</span></span>       |                                                                                                                                               |
| <span data-ttu-id="cbd0f-126">public void new(str cueGroupName)</span><span class="sxs-lookup"><span data-stu-id="cbd0f-126">public void new(str cueGroupName)</span></span>        | <span data-ttu-id="cbd0f-127">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-127">Initializes a new instance of the TreeNode class.</span></span>                                                                                             |

## <a name="method-changedby"></a><span data-ttu-id="cbd0f-128">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="cbd0f-128">Method changedBy</span></span>

<span data-ttu-id="cbd0f-129">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-129">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="cbd0f-130">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="cbd0f-130">Parameters - changedBy</span></span>

<span data-ttu-id="cbd0f-131">値</span><span class="sxs-lookup"><span data-stu-id="cbd0f-131">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="cbd0f-132">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="cbd0f-132">Return Value - changedBy</span></span>

<span data-ttu-id="cbd0f-133">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-133">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="cbd0f-134">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="cbd0f-134">Method changedDate</span></span>

<span data-ttu-id="cbd0f-135">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-135">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="cbd0f-136">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="cbd0f-136">Parameters - changedDate</span></span>

<span data-ttu-id="cbd0f-137">値</span><span class="sxs-lookup"><span data-stu-id="cbd0f-137">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="cbd0f-138">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="cbd0f-138">Return Value - changedDate</span></span>

<span data-ttu-id="cbd0f-139">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-139">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="cbd0f-140">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="cbd0f-140">Method changedTime</span></span>

<span data-ttu-id="cbd0f-141">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-141">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="cbd0f-142">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="cbd0f-142">Parameters - changedTime</span></span>

<span data-ttu-id="cbd0f-143">値</span><span class="sxs-lookup"><span data-stu-id="cbd0f-143">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="cbd0f-144">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="cbd0f-144">Return Value - changedTime</span></span>

<span data-ttu-id="cbd0f-145">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-145">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="cbd0f-146">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="cbd0f-146">Method createdBy</span></span>

<span data-ttu-id="cbd0f-147">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-147">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="cbd0f-148">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="cbd0f-148">Parameters - createdBy</span></span>

<span data-ttu-id="cbd0f-149">値</span><span class="sxs-lookup"><span data-stu-id="cbd0f-149">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="cbd0f-150">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="cbd0f-150">Return Value - createdBy</span></span>

<span data-ttu-id="cbd0f-151">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-151">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="cbd0f-152">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="cbd0f-152">Method creationDate</span></span>

<span data-ttu-id="cbd0f-153">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-153">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="cbd0f-154">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="cbd0f-154">Parameters - creationDate</span></span>

<span data-ttu-id="cbd0f-155">値</span><span class="sxs-lookup"><span data-stu-id="cbd0f-155">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="cbd0f-156">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="cbd0f-156">Return Value - creationDate</span></span>

<span data-ttu-id="cbd0f-157">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-157">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="cbd0f-158">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="cbd0f-158">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="cbd0f-159">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="cbd0f-159">Parameters - creationTime</span></span>

<span data-ttu-id="cbd0f-160">値</span><span class="sxs-lookup"><span data-stu-id="cbd0f-160">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="cbd0f-161">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="cbd0f-161">Return Value - creationTime</span></span>

## <a name="method-label"></a><span data-ttu-id="cbd0f-162">メソッド label</span><span class="sxs-lookup"><span data-stu-id="cbd0f-162">Method label</span></span>

<span data-ttu-id="cbd0f-163">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-163">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="cbd0f-164">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="cbd0f-164">Parameters - label</span></span>

<span data-ttu-id="cbd0f-165">値</span><span class="sxs-lookup"><span data-stu-id="cbd0f-165">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="cbd0f-166">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="cbd0f-166">Return Value - label</span></span>

<span data-ttu-id="cbd0f-167">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-167">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="cbd0f-168">備考 - label</span><span class="sxs-lookup"><span data-stu-id="cbd0f-168">Remarks - label</span></span>

<span data-ttu-id="cbd0f-169">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-169">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="cbd0f-170">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-170">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelid"></a><span data-ttu-id="cbd0f-171">メソッド LabelId</span><span class="sxs-lookup"><span data-stu-id="cbd0f-171">Method LabelId</span></span>

```xpp
public str LabelId()
```

### <a name="return-value---labelid"></a><span data-ttu-id="cbd0f-172">戻り値 - LabelId</span><span class="sxs-lookup"><span data-stu-id="cbd0f-172">Return Value - LabelId</span></span>

## <a name="method-name"></a><span data-ttu-id="cbd0f-173">メソッド名</span><span class="sxs-lookup"><span data-stu-id="cbd0f-173">Method name</span></span>

<span data-ttu-id="cbd0f-174">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-174">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="cbd0f-175">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="cbd0f-175">Parameters - name</span></span>

<span data-ttu-id="cbd0f-176">値</span><span class="sxs-lookup"><span data-stu-id="cbd0f-176">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="cbd0f-177">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="cbd0f-177">Return Value - name</span></span>

<span data-ttu-id="cbd0f-178">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-178">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="cbd0f-179">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="cbd0f-179">Remarks - name</span></span>

<span data-ttu-id="cbd0f-180">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-180">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="cbd0f-181">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-181">Begins with a letter.</span></span>
-   <span data-ttu-id="cbd0f-182">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-182">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="cbd0f-183">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-183">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="cbd0f-184">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-184">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="cbd0f-185">テーブルは、拡張データ型、基本列挙型、およびクラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-185">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, and classes.</span></span>

## <a name="method-origin"></a><span data-ttu-id="cbd0f-186">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="cbd0f-186">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="cbd0f-187">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="cbd0f-187">Parameters - origin</span></span>

<span data-ttu-id="cbd0f-188">値</span><span class="sxs-lookup"><span data-stu-id="cbd0f-188">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="cbd0f-189">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="cbd0f-189">Return Value - origin</span></span>

## <a name="method-new"></a><span data-ttu-id="cbd0f-190">メソッド new</span><span class="sxs-lookup"><span data-stu-id="cbd0f-190">Method new</span></span>

<span data-ttu-id="cbd0f-191">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="cbd0f-191">Initializes a new instance of the TreeNode class.</span></span>

```xpp
public void new(str cueGroupName)
```

### <a name="parameters---new"></a><span data-ttu-id="cbd0f-192">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="cbd0f-192">Parameters - new</span></span>

<span data-ttu-id="cbd0f-193">cueGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd0f-193">cueGroupName</span></span>  

