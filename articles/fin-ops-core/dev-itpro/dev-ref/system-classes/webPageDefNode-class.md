---
title: webPageDefNode クラス
description: このトピックでは、webPageDefNode クラスについて説明します。
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
ms.openlocfilehash: e914cd2b4640e9c6cbc333499053b73fc8a28087
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502685"
---
# <a name="class-webpagedefnode"></a><span data-ttu-id="e7ce5-103">クラス webPageDefNode</span><span class="sxs-lookup"><span data-stu-id="e7ce5-103">Class webPageDefNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class webPageDefNode extends TreeNode
```

<span data-ttu-id="e7ce5-104">webPageDefNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-104">The webPageDefNode class enables you to create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7ce5-105">備考</span><span class="sxs-lookup"><span data-stu-id="e7ce5-105">Remarks</span></span>

<span data-ttu-id="e7ce5-106">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-106">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="e7ce5-107">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-107">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

## <a name="examples"></a><span data-ttu-id="e7ce5-108">例</span><span class="sxs-lookup"><span data-stu-id="e7ce5-108">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="e7ce5-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="e7ce5-109">Methods</span></span>

| <span data-ttu-id="e7ce5-110">方法</span><span class="sxs-lookup"><span data-stu-id="e7ce5-110">Method</span></span>                                                     | <span data-ttu-id="e7ce5-111">説明</span><span class="sxs-lookup"><span data-stu-id="e7ce5-111">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ce5-112">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="e7ce5-112">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="e7ce5-113">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-113">Gets the source of the node.</span></span>                                                                                                              |
| <span data-ttu-id="e7ce5-114">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-114">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="e7ce5-115">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-115">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="e7ce5-116">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-116">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="e7ce5-117">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-117">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="e7ce5-118">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-118">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="e7ce5-119">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-119">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="e7ce5-120">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-120">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="e7ce5-121">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-121">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="e7ce5-122">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-122">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="e7ce5-123">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-123">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="e7ce5-124">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-124">public str creationTime(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="e7ce5-125">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-125">public str helpText(\[str value\])</span></span>                         | <span data-ttu-id="e7ce5-126">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-126">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="e7ce5-127">public str imageResource(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-127">public str imageResource(\[str value\])</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="e7ce5-128">public boolean mOSSOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-128">public boolean mOSSOnly(\[boolean value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="e7ce5-129">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-129">public str name(\[str value\])</span></span>                             | <span data-ttu-id="e7ce5-130">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-130">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="e7ce5-131">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-131">public Guid origin(\[Guid value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="e7ce5-132">public str pageTitle(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-132">public str pageTitle(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="e7ce5-133">public str parentPage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-133">public str parentPage(\[str value\])</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="e7ce5-134">public boolean publicPage(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-134">public boolean publicPage(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="e7ce5-135">public str uRL(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-135">public str uRL(\[str value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="e7ce5-136">public boolean useContext(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-136">public boolean useContext(\[boolean value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="e7ce5-137">public str webModule(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-137">public str webModule(\[str value\])</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="e7ce5-138">public str wSSHelpTopic(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-138">public str wSSHelpTopic(\[str value\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="e7ce5-139">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="e7ce5-139">public void new(str name)</span></span>                                  | <span data-ttu-id="e7ce5-140">新しい webPageDefNode の作成。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-140">Creates a new webPageDefNode.</span></span>                                                                                                             |
| <span data-ttu-id="e7ce5-141">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="e7ce5-141">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="e7ce5-142">指定した文字列に webPageDefNode のソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-142">Set the source of the webPageDefNode to the given string.</span></span>                                                                                 |

## <a name="method-aotgetsource"></a><span data-ttu-id="e7ce5-143">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="e7ce5-143">Method AOTgetSource</span></span>

<span data-ttu-id="e7ce5-144">ノードのソースを取得します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-144">Gets the source of the node.</span></span>

```xpp
public str AOTgetSource()
```

### <a name="return-value---aotgetsource"></a><span data-ttu-id="e7ce5-145">戻り値 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="e7ce5-145">Return Value - AOTgetSource</span></span>

<span data-ttu-id="e7ce5-146">ノードのソース。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-146">The source of the node.</span></span>

### <a name="remarks---aotgetsource"></a><span data-ttu-id="e7ce5-147">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="e7ce5-147">Remarks - AOTgetSource</span></span>

<span data-ttu-id="e7ce5-148">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-148">This method is overridden by nodes that have source code.</span></span>

## <a name="method-changedby"></a><span data-ttu-id="e7ce5-149">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="e7ce5-149">Method changedBy</span></span>

<span data-ttu-id="e7ce5-150">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-150">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="e7ce5-151">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="e7ce5-151">Parameters - changedBy</span></span>

<span data-ttu-id="e7ce5-152">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-152">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="e7ce5-153">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="e7ce5-153">Return Value - changedBy</span></span>

<span data-ttu-id="e7ce5-154">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-154">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="e7ce5-155">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="e7ce5-155">Method changedDate</span></span>

<span data-ttu-id="e7ce5-156">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-156">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="e7ce5-157">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="e7ce5-157">Parameters - changedDate</span></span>

<span data-ttu-id="e7ce5-158">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-158">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="e7ce5-159">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="e7ce5-159">Return Value - changedDate</span></span>

<span data-ttu-id="e7ce5-160">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-160">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="e7ce5-161">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="e7ce5-161">Method changedTime</span></span>

<span data-ttu-id="e7ce5-162">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-162">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="e7ce5-163">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="e7ce5-163">Parameters - changedTime</span></span>

<span data-ttu-id="e7ce5-164">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-164">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="e7ce5-165">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="e7ce5-165">Return Value - changedTime</span></span>

<span data-ttu-id="e7ce5-166">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-166">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="e7ce5-167">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="e7ce5-167">Method createdBy</span></span>

<span data-ttu-id="e7ce5-168">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-168">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="e7ce5-169">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="e7ce5-169">Parameters - createdBy</span></span>

<span data-ttu-id="e7ce5-170">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-170">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="e7ce5-171">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="e7ce5-171">Return Value - createdBy</span></span>

<span data-ttu-id="e7ce5-172">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-172">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="e7ce5-173">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="e7ce5-173">Method creationDate</span></span>

<span data-ttu-id="e7ce5-174">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-174">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="e7ce5-175">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="e7ce5-175">Parameters - creationDate</span></span>

<span data-ttu-id="e7ce5-176">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-176">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="e7ce5-177">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="e7ce5-177">Return Value - creationDate</span></span>

<span data-ttu-id="e7ce5-178">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-178">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="e7ce5-179">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="e7ce5-179">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="e7ce5-180">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="e7ce5-180">Parameters - creationTime</span></span>

<span data-ttu-id="e7ce5-181">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-181">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="e7ce5-182">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="e7ce5-182">Return Value - creationTime</span></span>

## <a name="method-helptext"></a><span data-ttu-id="e7ce5-183">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="e7ce5-183">Method helpText</span></span>

<span data-ttu-id="e7ce5-184">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-184">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="e7ce5-185">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="e7ce5-185">Parameters - helpText</span></span>

<span data-ttu-id="e7ce5-186">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-186">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="e7ce5-187">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="e7ce5-187">Return Value - helpText</span></span>

<span data-ttu-id="e7ce5-188">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-188">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="e7ce5-189">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="e7ce5-189">Remarks - helpText</span></span>

<span data-ttu-id="e7ce5-190">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-190">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="e7ce5-191">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-191">The help text must not exceed 250 characters.</span></span>

## <a name="method-imageresource"></a><span data-ttu-id="e7ce5-192">メソッド imageResource</span><span class="sxs-lookup"><span data-stu-id="e7ce5-192">Method imageResource</span></span>

```xpp
public str imageResource([str value])
```

### <a name="parameters---imageresource"></a><span data-ttu-id="e7ce5-193">パラメーター - imageResource</span><span class="sxs-lookup"><span data-stu-id="e7ce5-193">Parameters - imageResource</span></span>

<span data-ttu-id="e7ce5-194">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-194">value</span></span>  

### <a name="return-value---imageresource"></a><span data-ttu-id="e7ce5-195">戻り値 - imageResource</span><span class="sxs-lookup"><span data-stu-id="e7ce5-195">Return Value - imageResource</span></span>

## <a name="method-mossonly"></a><span data-ttu-id="e7ce5-196">メソッド mOSSOnly</span><span class="sxs-lookup"><span data-stu-id="e7ce5-196">Method mOSSOnly</span></span>

```xpp
public boolean mOSSOnly([boolean value])
```

### <a name="parameters---mossonly"></a><span data-ttu-id="e7ce5-197">パラメーター - mOSSOnly</span><span class="sxs-lookup"><span data-stu-id="e7ce5-197">Parameters - mOSSOnly</span></span>

<span data-ttu-id="e7ce5-198">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-198">value</span></span>  

### <a name="return-value---mossonly"></a><span data-ttu-id="e7ce5-199">戻り値 - mOSSOnly</span><span class="sxs-lookup"><span data-stu-id="e7ce5-199">Return Value - mOSSOnly</span></span>

## <a name="method-name"></a><span data-ttu-id="e7ce5-200">メソッド名</span><span class="sxs-lookup"><span data-stu-id="e7ce5-200">Method name</span></span>

<span data-ttu-id="e7ce5-201">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-201">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="e7ce5-202">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="e7ce5-202">Parameters - name</span></span>

<span data-ttu-id="e7ce5-203">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-203">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="e7ce5-204">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="e7ce5-204">Return Value - name</span></span>

<span data-ttu-id="e7ce5-205">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-205">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="e7ce5-206">備考 - name</span><span class="sxs-lookup"><span data-stu-id="e7ce5-206">Remarks - name</span></span>

<span data-ttu-id="e7ce5-207">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-207">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="e7ce5-208">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-208">Begins with a letter.</span></span>
-   <span data-ttu-id="e7ce5-209">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-209">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="e7ce5-210">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-210">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="e7ce5-211">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-211">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="e7ce5-212">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-212">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-origin"></a><span data-ttu-id="e7ce5-213">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="e7ce5-213">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="e7ce5-214">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="e7ce5-214">Parameters - origin</span></span>

<span data-ttu-id="e7ce5-215">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-215">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="e7ce5-216">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="e7ce5-216">Return Value - origin</span></span>

## <a name="method-pagetitle"></a><span data-ttu-id="e7ce5-217">メソッド pageTitle</span><span class="sxs-lookup"><span data-stu-id="e7ce5-217">Method pageTitle</span></span>

```xpp
public str pageTitle([str value])
```

### <a name="parameters---pagetitle"></a><span data-ttu-id="e7ce5-218">パラメーター - pageTitle</span><span class="sxs-lookup"><span data-stu-id="e7ce5-218">Parameters - pageTitle</span></span>

<span data-ttu-id="e7ce5-219">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-219">value</span></span>  

### <a name="return-value---pagetitle"></a><span data-ttu-id="e7ce5-220">戻り値 - pageTitle</span><span class="sxs-lookup"><span data-stu-id="e7ce5-220">Return Value - pageTitle</span></span>

## <a name="method-parentpage"></a><span data-ttu-id="e7ce5-221">メソッド parentPage</span><span class="sxs-lookup"><span data-stu-id="e7ce5-221">Method parentPage</span></span>

```xpp
public str parentPage([str value])
```

### <a name="parameters---parentpage"></a><span data-ttu-id="e7ce5-222">パラメーター - parentPage</span><span class="sxs-lookup"><span data-stu-id="e7ce5-222">Parameters - parentPage</span></span>

<span data-ttu-id="e7ce5-223">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-223">value</span></span>  

### <a name="return-value---parentpage"></a><span data-ttu-id="e7ce5-224">戻り値 - parentPage</span><span class="sxs-lookup"><span data-stu-id="e7ce5-224">Return Value - parentPage</span></span>

## <a name="method-publicpage"></a><span data-ttu-id="e7ce5-225">メソッド publicPage</span><span class="sxs-lookup"><span data-stu-id="e7ce5-225">Method publicPage</span></span>

```xpp
public boolean publicPage([boolean value])
```

### <a name="parameters---publicpage"></a><span data-ttu-id="e7ce5-226">パラメーター - publicPage</span><span class="sxs-lookup"><span data-stu-id="e7ce5-226">Parameters - publicPage</span></span>

<span data-ttu-id="e7ce5-227">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-227">value</span></span>  

### <a name="return-value---publicpage"></a><span data-ttu-id="e7ce5-228">戻り値 - publicPage</span><span class="sxs-lookup"><span data-stu-id="e7ce5-228">Return Value - publicPage</span></span>

## <a name="method-url"></a><span data-ttu-id="e7ce5-229">メソッド uRL</span><span class="sxs-lookup"><span data-stu-id="e7ce5-229">Method uRL</span></span>

```xpp
public str uRL([str value])
```

### <a name="parameters---url"></a><span data-ttu-id="e7ce5-230">パラメーター - uRL</span><span class="sxs-lookup"><span data-stu-id="e7ce5-230">Parameters - uRL</span></span>

<span data-ttu-id="e7ce5-231">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-231">value</span></span>  

### <a name="return-value---url"></a><span data-ttu-id="e7ce5-232">戻り値 - uRL</span><span class="sxs-lookup"><span data-stu-id="e7ce5-232">Return Value - uRL</span></span>

## <a name="method-usecontext"></a><span data-ttu-id="e7ce5-233">メソッド useContext</span><span class="sxs-lookup"><span data-stu-id="e7ce5-233">Method useContext</span></span>

```xpp
public boolean useContext([boolean value])
```

### <a name="parameters---usecontext"></a><span data-ttu-id="e7ce5-234">パラメーター - useContext</span><span class="sxs-lookup"><span data-stu-id="e7ce5-234">Parameters - useContext</span></span>

<span data-ttu-id="e7ce5-235">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-235">value</span></span>  

### <a name="return-value---usecontext"></a><span data-ttu-id="e7ce5-236">戻り値 - useContext</span><span class="sxs-lookup"><span data-stu-id="e7ce5-236">Return Value - useContext</span></span>

## <a name="method-webmodule"></a><span data-ttu-id="e7ce5-237">メソッド webModule</span><span class="sxs-lookup"><span data-stu-id="e7ce5-237">Method webModule</span></span>

```xpp
public str webModule([str value])
```

### <a name="parameters---webmodule"></a><span data-ttu-id="e7ce5-238">パラメーター - webModule</span><span class="sxs-lookup"><span data-stu-id="e7ce5-238">Parameters - webModule</span></span>

<span data-ttu-id="e7ce5-239">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-239">value</span></span>  

### <a name="return-value---webmodule"></a><span data-ttu-id="e7ce5-240">戻り値 - webModule</span><span class="sxs-lookup"><span data-stu-id="e7ce5-240">Return Value - webModule</span></span>

## <a name="method-wsshelptopic"></a><span data-ttu-id="e7ce5-241">メソッド wSSHelpTopic</span><span class="sxs-lookup"><span data-stu-id="e7ce5-241">Method wSSHelpTopic</span></span>

```xpp
public str wSSHelpTopic([str value])
```

### <a name="parameters---wsshelptopic"></a><span data-ttu-id="e7ce5-242">パラメーター - wSSHelpTopic</span><span class="sxs-lookup"><span data-stu-id="e7ce5-242">Parameters - wSSHelpTopic</span></span>

<span data-ttu-id="e7ce5-243">値</span><span class="sxs-lookup"><span data-stu-id="e7ce5-243">value</span></span>  

### <a name="return-value---wsshelptopic"></a><span data-ttu-id="e7ce5-244">戻り値 - wSSHelpTopic</span><span class="sxs-lookup"><span data-stu-id="e7ce5-244">Return Value - wSSHelpTopic</span></span>

## <a name="method-new"></a><span data-ttu-id="e7ce5-245">メソッド new</span><span class="sxs-lookup"><span data-stu-id="e7ce5-245">Method new</span></span>

<span data-ttu-id="e7ce5-246">新しい webPageDefNode の作成。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-246">Creates a new webPageDefNode.</span></span>

```xpp
public void new(str name)
```

### <a name="parameters---new"></a><span data-ttu-id="e7ce5-247">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="e7ce5-247">Parameters - new</span></span>

<span data-ttu-id="e7ce5-248">名前</span><span class="sxs-lookup"><span data-stu-id="e7ce5-248">name</span></span>  

## <a name="method-aotsetsource"></a><span data-ttu-id="e7ce5-249">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="e7ce5-249">Method AOTsetSource</span></span>

<span data-ttu-id="e7ce5-250">指定した文字列に webPageDefNode のソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-250">Set the source of the webPageDefNode to the given string.</span></span>

```xpp
public void AOTsetSource(str source, [boolean isStatic])
```

### <a name="parameters---aotsetsource"></a><span data-ttu-id="e7ce5-251">パラメーター - AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="e7ce5-251">Parameters - AOTsetSource</span></span>

<span data-ttu-id="e7ce5-252">ソース</span><span class="sxs-lookup"><span data-stu-id="e7ce5-252">source</span></span>  
<span data-ttu-id="e7ce5-253">ソースが静的であるかどうかのマークを付けるオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-253">Optional parameter marking if the source provided is static.</span></span>

<!-- -->

<span data-ttu-id="e7ce5-254">isStatic</span><span class="sxs-lookup"><span data-stu-id="e7ce5-254">isStatic</span></span>  
<span data-ttu-id="e7ce5-255">ソースが静的であるかどうかのマークを付けるオプションのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-255">Optional parameter marking if the source provided is static.</span></span>

### <a name="remarks---aotsetsource"></a><span data-ttu-id="e7ce5-256">備考 - AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="e7ce5-256">Remarks - AOTsetSource</span></span>

<span data-ttu-id="e7ce5-257">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="e7ce5-257">This method is overridden by nodes which have source code.</span></span>

