---
title: HelpDocSetNode クラス
description: このトピックでは、HelpDocSetNode クラスについて説明します。
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
ms.openlocfilehash: d9637d35fd5e4cbe88a582bab181a250978f841e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502609"
---
# <a name="class-helpdocsetnode"></a><span data-ttu-id="be4d3-103">クラス HelpDocSetNode</span><span class="sxs-lookup"><span data-stu-id="be4d3-103">Class HelpDocSetNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class HelpDocSetNode extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="be4d3-104">備考</span><span class="sxs-lookup"><span data-stu-id="be4d3-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="be4d3-105">例</span><span class="sxs-lookup"><span data-stu-id="be4d3-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="be4d3-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="be4d3-106">Methods</span></span>

| <span data-ttu-id="be4d3-107">方法</span><span class="sxs-lookup"><span data-stu-id="be4d3-107">Method</span></span>                                                     | <span data-ttu-id="be4d3-108">説明</span><span class="sxs-lookup"><span data-stu-id="be4d3-108">Description</span></span>                                                                |
|------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="be4d3-109">public boolean addToApplicationHelpMenu(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-109">public boolean addToApplicationHelpMenu(\[boolean value\])</span></span> |                                                                            |
| <span data-ttu-id="be4d3-110">public boolean addToDeveloperHelpMenu(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-110">public boolean addToDeveloperHelpMenu(\[boolean value\])</span></span>   |                                                                            |
| <span data-ttu-id="be4d3-111">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-111">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="be4d3-112">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="be4d3-112">Gets or sets the name of the user who last changed the application object.</span></span> |
| <span data-ttu-id="be4d3-113">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-113">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="be4d3-114">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="be4d3-114">Gets or sets the date an application object was last changed.</span></span>              |
| <span data-ttu-id="be4d3-115">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-115">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="be4d3-116">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="be4d3-116">Gets or sets the time an application object was last changed.</span></span>              |
| <span data-ttu-id="be4d3-117">public int contentLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-117">public int contentLocation(\[int value\])</span></span>                  |                                                                            |
| <span data-ttu-id="be4d3-118">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-118">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="be4d3-119">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="be4d3-119">Gets or sets the name of the user who created the application object.</span></span>      |
| <span data-ttu-id="be4d3-120">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-120">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="be4d3-121">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="be4d3-121">Gets or sets the date an application object was created.</span></span>                   |
| <span data-ttu-id="be4d3-122">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-122">public str creationTime(\[str value\])</span></span>                     |                                                                            |
| <span data-ttu-id="be4d3-123">public boolean developerDocumentSet(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-123">public boolean developerDocumentSet(\[boolean value\])</span></span>     |                                                                            |
| <span data-ttu-id="be4d3-124">public str documentSetDescription(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-124">public str documentSetDescription(\[str value\])</span></span>           |                                                                            |
| <span data-ttu-id="be4d3-125">public str documentSetName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-125">public str documentSetName(\[str value\])</span></span>                  |                                                                            |
| <span data-ttu-id="be4d3-126">public str helpProviderClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-126">public str helpProviderClass(\[str value\])</span></span>                |                                                                            |
| <span data-ttu-id="be4d3-127">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-127">public Guid origin(\[Guid value\])</span></span>                         |                                                                            |
| <span data-ttu-id="be4d3-128">public boolean userDocumentSet(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="be4d3-128">public boolean userDocumentSet(\[boolean value\])</span></span>          |                                                                            |
| <span data-ttu-id="be4d3-129">public void new(str DocSetName)</span><span class="sxs-lookup"><span data-stu-id="be4d3-129">public void new(str DocSetName)</span></span>                            | <span data-ttu-id="be4d3-130">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="be4d3-130">Initializes a new instance of the TreeNode class.</span></span>                          |

## <a name="method-addtoapplicationhelpmenu"></a><span data-ttu-id="be4d3-131">メソッド addToApplicationHelpMenu</span><span class="sxs-lookup"><span data-stu-id="be4d3-131">Method addToApplicationHelpMenu</span></span>

```xpp
public boolean addToApplicationHelpMenu([boolean value])
```

### <a name="parameters---addtoapplicationhelpmenu"></a><span data-ttu-id="be4d3-132">パラメーター - addToApplicationHelpMenu</span><span class="sxs-lookup"><span data-stu-id="be4d3-132">Parameters - addToApplicationHelpMenu</span></span>

<span data-ttu-id="be4d3-133">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-133">value</span></span>  

### <a name="return-value---addtoapplicationhelpmenu"></a><span data-ttu-id="be4d3-134">戻り値 - addToApplicationHelpMenu</span><span class="sxs-lookup"><span data-stu-id="be4d3-134">Return Value - addToApplicationHelpMenu</span></span>

## <a name="method-addtodeveloperhelpmenu"></a><span data-ttu-id="be4d3-135">メソッド addToDeveloperHelpMenu</span><span class="sxs-lookup"><span data-stu-id="be4d3-135">Method addToDeveloperHelpMenu</span></span>

```xpp
public boolean addToDeveloperHelpMenu([boolean value])
```

### <a name="parameters---addtodeveloperhelpmenu"></a><span data-ttu-id="be4d3-136">パラメーター - addToDeveloperHelpMenu</span><span class="sxs-lookup"><span data-stu-id="be4d3-136">Parameters - addToDeveloperHelpMenu</span></span>

<span data-ttu-id="be4d3-137">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-137">value</span></span>  

### <a name="return-value---addtodeveloperhelpmenu"></a><span data-ttu-id="be4d3-138">戻り値 - addToDeveloperHelpMenu</span><span class="sxs-lookup"><span data-stu-id="be4d3-138">Return Value - addToDeveloperHelpMenu</span></span>

## <a name="method-changedby"></a><span data-ttu-id="be4d3-139">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="be4d3-139">Method changedBy</span></span>

<span data-ttu-id="be4d3-140">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="be4d3-140">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="be4d3-141">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="be4d3-141">Parameters - changedBy</span></span>

<span data-ttu-id="be4d3-142">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-142">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="be4d3-143">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="be4d3-143">Return Value - changedBy</span></span>

<span data-ttu-id="be4d3-144">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="be4d3-144">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="be4d3-145">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="be4d3-145">Method changedDate</span></span>

<span data-ttu-id="be4d3-146">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="be4d3-146">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="be4d3-147">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="be4d3-147">Parameters - changedDate</span></span>

<span data-ttu-id="be4d3-148">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-148">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="be4d3-149">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="be4d3-149">Return Value - changedDate</span></span>

<span data-ttu-id="be4d3-150">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="be4d3-150">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="be4d3-151">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="be4d3-151">Method changedTime</span></span>

<span data-ttu-id="be4d3-152">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="be4d3-152">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="be4d3-153">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="be4d3-153">Parameters - changedTime</span></span>

<span data-ttu-id="be4d3-154">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-154">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="be4d3-155">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="be4d3-155">Return Value - changedTime</span></span>

<span data-ttu-id="be4d3-156">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="be4d3-156">The time an application object was last changed.</span></span>

## <a name="method-contentlocation"></a><span data-ttu-id="be4d3-157">メソッド contentLocation</span><span class="sxs-lookup"><span data-stu-id="be4d3-157">Method contentLocation</span></span>

```xpp
public int contentLocation([int value])
```

### <a name="parameters---contentlocation"></a><span data-ttu-id="be4d3-158">パラメーター - contentLocation</span><span class="sxs-lookup"><span data-stu-id="be4d3-158">Parameters - contentLocation</span></span>

<span data-ttu-id="be4d3-159">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-159">value</span></span>  

### <a name="return-value---contentlocation"></a><span data-ttu-id="be4d3-160">戻り値 - contentLocation</span><span class="sxs-lookup"><span data-stu-id="be4d3-160">Return Value - contentLocation</span></span>

## <a name="method-createdby"></a><span data-ttu-id="be4d3-161">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="be4d3-161">Method createdBy</span></span>

<span data-ttu-id="be4d3-162">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="be4d3-162">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="be4d3-163">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="be4d3-163">Parameters - createdBy</span></span>

<span data-ttu-id="be4d3-164">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-164">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="be4d3-165">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="be4d3-165">Return Value - createdBy</span></span>

<span data-ttu-id="be4d3-166">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="be4d3-166">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="be4d3-167">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="be4d3-167">Method creationDate</span></span>

<span data-ttu-id="be4d3-168">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="be4d3-168">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="be4d3-169">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="be4d3-169">Parameters - creationDate</span></span>

<span data-ttu-id="be4d3-170">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-170">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="be4d3-171">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="be4d3-171">Return Value - creationDate</span></span>

<span data-ttu-id="be4d3-172">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="be4d3-172">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="be4d3-173">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="be4d3-173">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="be4d3-174">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="be4d3-174">Parameters - creationTime</span></span>

<span data-ttu-id="be4d3-175">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-175">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="be4d3-176">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="be4d3-176">Return Value - creationTime</span></span>

## <a name="method-developerdocumentset"></a><span data-ttu-id="be4d3-177">メソッド developerDocumentSet</span><span class="sxs-lookup"><span data-stu-id="be4d3-177">Method developerDocumentSet</span></span>

```xpp
public boolean developerDocumentSet([boolean value])
```

### <a name="parameters---developerdocumentset"></a><span data-ttu-id="be4d3-178">パラメーター - developerDocumentSet</span><span class="sxs-lookup"><span data-stu-id="be4d3-178">Parameters - developerDocumentSet</span></span>

<span data-ttu-id="be4d3-179">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-179">value</span></span>  

### <a name="return-value---developerdocumentset"></a><span data-ttu-id="be4d3-180">戻り値 - developerDocumentSet</span><span class="sxs-lookup"><span data-stu-id="be4d3-180">Return Value - developerDocumentSet</span></span>

## <a name="method-documentsetdescription"></a><span data-ttu-id="be4d3-181">メソッド documentSetDescription</span><span class="sxs-lookup"><span data-stu-id="be4d3-181">Method documentSetDescription</span></span>

```xpp
public str documentSetDescription([str value])
```

### <a name="parameters---documentsetdescription"></a><span data-ttu-id="be4d3-182">パラメーター - documentSetDescription</span><span class="sxs-lookup"><span data-stu-id="be4d3-182">Parameters - documentSetDescription</span></span>

<span data-ttu-id="be4d3-183">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-183">value</span></span>  

### <a name="return-value---documentsetdescription"></a><span data-ttu-id="be4d3-184">戻り値 - documentSetDescription</span><span class="sxs-lookup"><span data-stu-id="be4d3-184">Return Value - documentSetDescription</span></span>

## <a name="method-documentsetname"></a><span data-ttu-id="be4d3-185">メソッド documentSetName</span><span class="sxs-lookup"><span data-stu-id="be4d3-185">Method documentSetName</span></span>

```xpp
public str documentSetName([str value])
```

### <a name="parameters---documentsetname"></a><span data-ttu-id="be4d3-186">パラメーター - documentSetName</span><span class="sxs-lookup"><span data-stu-id="be4d3-186">Parameters - documentSetName</span></span>

<span data-ttu-id="be4d3-187">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-187">value</span></span>  

### <a name="return-value---documentsetname"></a><span data-ttu-id="be4d3-188">戻り値 - documentSetName</span><span class="sxs-lookup"><span data-stu-id="be4d3-188">Return Value - documentSetName</span></span>

## <a name="method-helpproviderclass"></a><span data-ttu-id="be4d3-189">メソッド helpProviderClass</span><span class="sxs-lookup"><span data-stu-id="be4d3-189">Method helpProviderClass</span></span>

```xpp
public str helpProviderClass([str value])
```

### <a name="parameters---helpproviderclass"></a><span data-ttu-id="be4d3-190">パラメーター - helpProviderClass</span><span class="sxs-lookup"><span data-stu-id="be4d3-190">Parameters - helpProviderClass</span></span>

<span data-ttu-id="be4d3-191">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-191">value</span></span>  

### <a name="return-value---helpproviderclass"></a><span data-ttu-id="be4d3-192">戻り値 - helpProviderClass</span><span class="sxs-lookup"><span data-stu-id="be4d3-192">Return Value - helpProviderClass</span></span>

## <a name="method-origin"></a><span data-ttu-id="be4d3-193">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="be4d3-193">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="be4d3-194">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="be4d3-194">Parameters - origin</span></span>

<span data-ttu-id="be4d3-195">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-195">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="be4d3-196">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="be4d3-196">Return Value - origin</span></span>

## <a name="method-userdocumentset"></a><span data-ttu-id="be4d3-197">メソッド userDocumentSet</span><span class="sxs-lookup"><span data-stu-id="be4d3-197">Method userDocumentSet</span></span>

```xpp
public boolean userDocumentSet([boolean value])
```

### <a name="parameters---userdocumentset"></a><span data-ttu-id="be4d3-198">パラメーター - userDocumentSet</span><span class="sxs-lookup"><span data-stu-id="be4d3-198">Parameters - userDocumentSet</span></span>

<span data-ttu-id="be4d3-199">値</span><span class="sxs-lookup"><span data-stu-id="be4d3-199">value</span></span>  

### <a name="return-value---userdocumentset"></a><span data-ttu-id="be4d3-200">戻り値 - userDocumentSet</span><span class="sxs-lookup"><span data-stu-id="be4d3-200">Return Value - userDocumentSet</span></span>

## <a name="method-new"></a><span data-ttu-id="be4d3-201">メソッド new</span><span class="sxs-lookup"><span data-stu-id="be4d3-201">Method new</span></span>

<span data-ttu-id="be4d3-202">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="be4d3-202">Initializes a new instance of the TreeNode class.</span></span>

```xpp
public void new(str DocSetName)
```

### <a name="parameters---new"></a><span data-ttu-id="be4d3-203">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="be4d3-203">Parameters - new</span></span>

<span data-ttu-id="be4d3-204">DocSetName</span><span class="sxs-lookup"><span data-stu-id="be4d3-204">DocSetName</span></span>  

