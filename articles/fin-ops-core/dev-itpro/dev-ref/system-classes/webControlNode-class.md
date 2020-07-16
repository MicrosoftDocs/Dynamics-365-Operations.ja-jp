---
title: webControlNode クラス
description: このトピックでは、webControlNode クラスについて説明します。
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
ms.openlocfilehash: 279dbf5d25d96f0986272270272888fe755f6ad2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502999"
---
# <a name="class-webcontrolnode"></a><span data-ttu-id="b29cb-103">クラス webControlNode</span><span class="sxs-lookup"><span data-stu-id="b29cb-103">Class webControlNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class webControlNode extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="b29cb-104">備考</span><span class="sxs-lookup"><span data-stu-id="b29cb-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="b29cb-105">例</span><span class="sxs-lookup"><span data-stu-id="b29cb-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b29cb-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="b29cb-106">Methods</span></span>

| <span data-ttu-id="b29cb-107">方法</span><span class="sxs-lookup"><span data-stu-id="b29cb-107">Method</span></span>                                                        | <span data-ttu-id="b29cb-108">説明</span><span class="sxs-lookup"><span data-stu-id="b29cb-108">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b29cb-109">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="b29cb-109">public str AOTgetSource()</span></span>                                     | <span data-ttu-id="b29cb-110">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-110">Returns the source code of this node.</span></span>                                                                                                         |
| <span data-ttu-id="b29cb-111">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b29cb-111">public str changedBy(\[str value\])</span></span>                           | <span data-ttu-id="b29cb-112">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-112">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="b29cb-113">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="b29cb-113">public Date changedDate(\[Date value\])</span></span>                       | <span data-ttu-id="b29cb-114">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-114">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="b29cb-115">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b29cb-115">public str changedTime(\[str value\])</span></span>                         | <span data-ttu-id="b29cb-116">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-116">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="b29cb-117">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b29cb-117">public str createdBy(\[str value\])</span></span>                           | <span data-ttu-id="b29cb-118">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-118">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="b29cb-119">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="b29cb-119">public Date creationDate(\[Date value\])</span></span>                      | <span data-ttu-id="b29cb-120">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-120">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="b29cb-121">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b29cb-121">public str creationTime(\[str value\])</span></span>                        |                                                                                                                                               |
| <span data-ttu-id="b29cb-122">public str filename(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b29cb-122">public str filename(\[str value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="b29cb-123">public List getRelatedWebControls(\[boolean firstLevelOnly\])</span><span class="sxs-lookup"><span data-stu-id="b29cb-123">public List getRelatedWebControls(\[boolean firstLevelOnly\])</span></span> | <span data-ttu-id="b29cb-124">この Web コントロールに関連する Web コントロールの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-124">Get a list of web controls that are related to this web control.</span></span>                                                                              |
| <span data-ttu-id="b29cb-125">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b29cb-125">public str helpText(\[str value\])</span></span>                            | <span data-ttu-id="b29cb-126">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-126">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="b29cb-127">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b29cb-127">public str name(\[str value\])</span></span>                                | <span data-ttu-id="b29cb-128">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-128">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="b29cb-129">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="b29cb-129">public Guid origin(\[Guid value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="b29cb-130">public str relativePath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b29cb-130">public str relativePath(\[str value\])</span></span>                        |                                                                                                                                               |
| <span data-ttu-id="b29cb-131">public str version(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b29cb-131">public str version(\[str value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="b29cb-132">::public static webControlNode createFromFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="b29cb-132">::public static webControlNode createFromFile(str fileName)</span></span>   |                                                                                                                                               |
| <span data-ttu-id="b29cb-133">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="b29cb-133">public void AOTsetSource(str source, \[boolean isStatic\])</span></span>    | <span data-ttu-id="b29cb-134">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-134">Sets the source code of this node.</span></span>                                                                                                            |

## <a name="method-aotgetsource"></a><span data-ttu-id="b29cb-135">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="b29cb-135">Method AOTgetSource</span></span>

<span data-ttu-id="b29cb-136">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-136">Returns the source code of this node.</span></span>

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a><span data-ttu-id="b29cb-137">戻り値 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="b29cb-137">Return Value - AOTgetSource</span></span>

<span data-ttu-id="b29cb-138">ソース コードが含まれている文字列が存在する場合。それ以外の場合は nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="b29cb-138">The string that contains source code, if there is any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="remarks---aotgetsource"></a><span data-ttu-id="b29cb-139">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="b29cb-139">Remarks - AOTgetSource</span></span>

<span data-ttu-id="b29cb-140">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="b29cb-140">This function is overridden by nodes that have source code.</span></span>

## <a name="method-changedby"></a><span data-ttu-id="b29cb-141">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="b29cb-141">Method changedBy</span></span>

<span data-ttu-id="b29cb-142">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-142">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="b29cb-143">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="b29cb-143">Parameters - changedBy</span></span>

<span data-ttu-id="b29cb-144">値</span><span class="sxs-lookup"><span data-stu-id="b29cb-144">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="b29cb-145">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="b29cb-145">Return Value - changedBy</span></span>

<span data-ttu-id="b29cb-146">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="b29cb-146">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="b29cb-147">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="b29cb-147">Method changedDate</span></span>

<span data-ttu-id="b29cb-148">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-148">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="b29cb-149">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="b29cb-149">Parameters - changedDate</span></span>

<span data-ttu-id="b29cb-150">値</span><span class="sxs-lookup"><span data-stu-id="b29cb-150">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="b29cb-151">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="b29cb-151">Return Value - changedDate</span></span>

<span data-ttu-id="b29cb-152">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="b29cb-152">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="b29cb-153">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="b29cb-153">Method changedTime</span></span>

<span data-ttu-id="b29cb-154">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-154">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="b29cb-155">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="b29cb-155">Parameters - changedTime</span></span>

<span data-ttu-id="b29cb-156">値</span><span class="sxs-lookup"><span data-stu-id="b29cb-156">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="b29cb-157">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="b29cb-157">Return Value - changedTime</span></span>

<span data-ttu-id="b29cb-158">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="b29cb-158">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="b29cb-159">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="b29cb-159">Method createdBy</span></span>

<span data-ttu-id="b29cb-160">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-160">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="b29cb-161">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="b29cb-161">Parameters - createdBy</span></span>

<span data-ttu-id="b29cb-162">値</span><span class="sxs-lookup"><span data-stu-id="b29cb-162">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="b29cb-163">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="b29cb-163">Return Value - createdBy</span></span>

<span data-ttu-id="b29cb-164">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="b29cb-164">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="b29cb-165">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="b29cb-165">Method creationDate</span></span>

<span data-ttu-id="b29cb-166">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-166">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="b29cb-167">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="b29cb-167">Parameters - creationDate</span></span>

<span data-ttu-id="b29cb-168">値</span><span class="sxs-lookup"><span data-stu-id="b29cb-168">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="b29cb-169">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="b29cb-169">Return Value - creationDate</span></span>

<span data-ttu-id="b29cb-170">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="b29cb-170">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="b29cb-171">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="b29cb-171">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="b29cb-172">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="b29cb-172">Parameters - creationTime</span></span>

<span data-ttu-id="b29cb-173">値</span><span class="sxs-lookup"><span data-stu-id="b29cb-173">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="b29cb-174">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="b29cb-174">Return Value - creationTime</span></span>

## <a name="method-filename"></a><span data-ttu-id="b29cb-175">メソッド filename</span><span class="sxs-lookup"><span data-stu-id="b29cb-175">Method filename</span></span>

```xpp
public str filename([str value])
```

### <a name="parameters---filename"></a><span data-ttu-id="b29cb-176">パラメーター - filename</span><span class="sxs-lookup"><span data-stu-id="b29cb-176">Parameters - filename</span></span>

<span data-ttu-id="b29cb-177">値</span><span class="sxs-lookup"><span data-stu-id="b29cb-177">value</span></span>  

### <a name="return-value---filename"></a><span data-ttu-id="b29cb-178">戻り値 - filename</span><span class="sxs-lookup"><span data-stu-id="b29cb-178">Return Value - filename</span></span>

## <a name="method-getrelatedwebcontrols"></a><span data-ttu-id="b29cb-179">メソッド getRelatedWebControls</span><span class="sxs-lookup"><span data-stu-id="b29cb-179">Method getRelatedWebControls</span></span>

<span data-ttu-id="b29cb-180">この Web コントロールに関連する Web コントロールの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-180">Get a list of web controls that are related to this web control.</span></span>

```xpp
public List getRelatedWebControls([boolean firstLevelOnly])
```

### <a name="parameters---getrelatedwebcontrols"></a><span data-ttu-id="b29cb-181">パラメーター - getRelatedWebControls</span><span class="sxs-lookup"><span data-stu-id="b29cb-181">Parameters - getRelatedWebControls</span></span>

<span data-ttu-id="b29cb-182">firstLevelOnly</span><span class="sxs-lookup"><span data-stu-id="b29cb-182">firstLevelOnly</span></span>  
<span data-ttu-id="b29cb-183">Web コントロールの最初のレベルのみがオンになっているかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="b29cb-183">A value that indicates whether only the first level of web controls is checked.</span></span>

### <a name="return-value---getrelatedwebcontrols"></a><span data-ttu-id="b29cb-184">戻り値 - getRelatedWebControls</span><span class="sxs-lookup"><span data-stu-id="b29cb-184">Return Value - getRelatedWebControls</span></span>

<span data-ttu-id="b29cb-185">関連する Web コントロールの一覧。</span><span class="sxs-lookup"><span data-stu-id="b29cb-185">A list of related web controls.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="b29cb-186">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="b29cb-186">Method helpText</span></span>

<span data-ttu-id="b29cb-187">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-187">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="b29cb-188">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="b29cb-188">Parameters - helpText</span></span>

<span data-ttu-id="b29cb-189">値</span><span class="sxs-lookup"><span data-stu-id="b29cb-189">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="b29cb-190">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="b29cb-190">Return Value - helpText</span></span>

<span data-ttu-id="b29cb-191">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="b29cb-191">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="b29cb-192">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="b29cb-192">Remarks - helpText</span></span>

<span data-ttu-id="b29cb-193">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-193">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="b29cb-194">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="b29cb-194">The help text must not exceed 250 characters.</span></span>

## <a name="method-name"></a><span data-ttu-id="b29cb-195">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b29cb-195">Method name</span></span>

<span data-ttu-id="b29cb-196">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-196">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="b29cb-197">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="b29cb-197">Parameters - name</span></span>

<span data-ttu-id="b29cb-198">値</span><span class="sxs-lookup"><span data-stu-id="b29cb-198">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="b29cb-199">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="b29cb-199">Return Value - name</span></span>

<span data-ttu-id="b29cb-200">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="b29cb-200">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="b29cb-201">備考 - name</span><span class="sxs-lookup"><span data-stu-id="b29cb-201">Remarks - name</span></span>

<span data-ttu-id="b29cb-202">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b29cb-202">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="b29cb-203">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="b29cb-203">Begins with a letter.</span></span>
-   <span data-ttu-id="b29cb-204">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="b29cb-204">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="b29cb-205">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b29cb-205">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="b29cb-206">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="b29cb-206">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="b29cb-207">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="b29cb-207">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-origin"></a><span data-ttu-id="b29cb-208">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="b29cb-208">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="b29cb-209">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="b29cb-209">Parameters - origin</span></span>

<span data-ttu-id="b29cb-210">値</span><span class="sxs-lookup"><span data-stu-id="b29cb-210">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="b29cb-211">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="b29cb-211">Return Value - origin</span></span>

## <a name="method-relativepath"></a><span data-ttu-id="b29cb-212">メソッド relativePath</span><span class="sxs-lookup"><span data-stu-id="b29cb-212">Method relativePath</span></span>

```xpp
public str relativePath([str value])
```

### <a name="parameters---relativepath"></a><span data-ttu-id="b29cb-213">パラメーター - relativePath</span><span class="sxs-lookup"><span data-stu-id="b29cb-213">Parameters - relativePath</span></span>

<span data-ttu-id="b29cb-214">値</span><span class="sxs-lookup"><span data-stu-id="b29cb-214">value</span></span>  

### <a name="return-value---relativepath"></a><span data-ttu-id="b29cb-215">戻り値 - relativePath</span><span class="sxs-lookup"><span data-stu-id="b29cb-215">Return Value - relativePath</span></span>

## <a name="method-version"></a><span data-ttu-id="b29cb-216">メソッド version</span><span class="sxs-lookup"><span data-stu-id="b29cb-216">Method version</span></span>

```xpp
public str version([str value])
```

### <a name="parameters---version"></a><span data-ttu-id="b29cb-217">パラメーター - version</span><span class="sxs-lookup"><span data-stu-id="b29cb-217">Parameters - version</span></span>

<span data-ttu-id="b29cb-218">値</span><span class="sxs-lookup"><span data-stu-id="b29cb-218">value</span></span>  

### <a name="return-value---version"></a><span data-ttu-id="b29cb-219">戻り値 - version</span><span class="sxs-lookup"><span data-stu-id="b29cb-219">Return Value - version</span></span>

## <a name="method-createfromfile"></a><span data-ttu-id="b29cb-220">メソッド createFromFile</span><span class="sxs-lookup"><span data-stu-id="b29cb-220">Method createFromFile</span></span>

```xpp
public static webControlNode createFromFile(str fileName)
```

### <a name="parameters---createfromfile"></a><span data-ttu-id="b29cb-221">パラメータ - createFromFile</span><span class="sxs-lookup"><span data-stu-id="b29cb-221">Parameters - createFromFile</span></span>

<span data-ttu-id="b29cb-222">fileName</span><span class="sxs-lookup"><span data-stu-id="b29cb-222">fileName</span></span>  

### <a name="return-value---createfromfile"></a><span data-ttu-id="b29cb-223">戻り値 - createFromFile</span><span class="sxs-lookup"><span data-stu-id="b29cb-223">Return Value - createFromFile</span></span>

## <a name="method-aotsetsource"></a><span data-ttu-id="b29cb-224">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="b29cb-224">Method AOTsetSource</span></span>

<span data-ttu-id="b29cb-225">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="b29cb-225">Sets the source code of this node.</span></span>

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a><span data-ttu-id="b29cb-226">パラメーター - AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="b29cb-226">Parameters - AOTsetSource</span></span>

<span data-ttu-id="b29cb-227">ソース</span><span class="sxs-lookup"><span data-stu-id="b29cb-227">source</span></span>  
<span data-ttu-id="b29cb-228">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b29cb-228">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="b29cb-229">isStatic</span><span class="sxs-lookup"><span data-stu-id="b29cb-229">isStatic</span></span>  
<span data-ttu-id="b29cb-230">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="b29cb-230">The value that specifies whether the method is static; optional.</span></span>

### <a name="remarks---aotsetsource"></a><span data-ttu-id="b29cb-231">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="b29cb-231">Remarks - AOTsetSource</span></span>

<span data-ttu-id="b29cb-232">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="b29cb-232">This method is overridden by nodes that have source code.</span></span>

