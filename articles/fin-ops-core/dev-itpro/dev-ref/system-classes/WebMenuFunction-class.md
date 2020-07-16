---
title: WebMenuFunction クラス
description: このトピックでは、WebMenuFunction クラスについて説明します。
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
ms.openlocfilehash: 2034d91f2cd343f8af221804b0c2e357cdb5f850
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503002"
---
# <a name="class-webmenufunction"></a><span data-ttu-id="7b8c9-103">クラス WebMenuFunction</span><span class="sxs-lookup"><span data-stu-id="7b8c9-103">Class WebMenuFunction</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class WebMenuFunction extends SecureNode
```

<span data-ttu-id="7b8c9-104">WebMenuFunction クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-104">The WebMenuFunction class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b8c9-105">備考</span><span class="sxs-lookup"><span data-stu-id="7b8c9-105">Remarks</span></span>

<span data-ttu-id="7b8c9-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="7b8c9-107">例</span><span class="sxs-lookup"><span data-stu-id="7b8c9-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="7b8c9-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b8c9-108">Methods</span></span>

| <span data-ttu-id="7b8c9-109">方法</span><span class="sxs-lookup"><span data-stu-id="7b8c9-109">Method</span></span>                                                                                           | <span data-ttu-id="7b8c9-110">説明</span><span class="sxs-lookup"><span data-stu-id="7b8c9-110">Description</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b8c9-111">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b8c9-111">public str changedBy(\[str value\])</span></span>                                                              | <span data-ttu-id="7b8c9-112">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-112">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="7b8c9-113">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b8c9-113">public Date changedDate(\[Date value\])</span></span>                                                          | <span data-ttu-id="7b8c9-114">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-114">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="7b8c9-115">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b8c9-115">public str changedTime(\[str value\])</span></span>                                                            | <span data-ttu-id="7b8c9-116">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-116">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="7b8c9-117">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b8c9-117">public str createdBy(\[str value\])</span></span>                                                              | <span data-ttu-id="7b8c9-118">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-118">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="7b8c9-119">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7b8c9-119">public Date creationDate(\[Date value\])</span></span>                                                         | <span data-ttu-id="7b8c9-120">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-120">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="7b8c9-121">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b8c9-121">public str creationTime(\[str value\])</span></span>                                                           |                                                                                                                                               |
| <span data-ttu-id="7b8c9-122">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b8c9-122">public str helpText(\[str value\])</span></span>                                                               | <span data-ttu-id="7b8c9-123">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-123">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="7b8c9-124">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b8c9-124">public str label(\[str value\])</span></span>                                                                  | <span data-ttu-id="7b8c9-125">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-125">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="7b8c9-126">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b8c9-126">public str name(\[str value\])</span></span>                                                                   | <span data-ttu-id="7b8c9-127">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-127">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="7b8c9-128">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="7b8c9-128">public Guid origin(\[Guid value\])</span></span>                                                               |                                                                                                                                               |
| <span data-ttu-id="7b8c9-129">::public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)</span><span class="sxs-lookup"><span data-stu-id="7b8c9-129">::public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)</span></span> |                                                                                                                                               |

## <a name="method-changedby"></a><span data-ttu-id="7b8c9-130">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="7b8c9-130">Method changedBy</span></span>

<span data-ttu-id="7b8c9-131">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-131">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="7b8c9-132">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="7b8c9-132">Parameters - changedBy</span></span>

<span data-ttu-id="7b8c9-133">値</span><span class="sxs-lookup"><span data-stu-id="7b8c9-133">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="7b8c9-134">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="7b8c9-134">Return Value - changedBy</span></span>

<span data-ttu-id="7b8c9-135">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-135">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="7b8c9-136">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="7b8c9-136">Method changedDate</span></span>

<span data-ttu-id="7b8c9-137">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-137">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="7b8c9-138">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="7b8c9-138">Parameters - changedDate</span></span>

<span data-ttu-id="7b8c9-139">値</span><span class="sxs-lookup"><span data-stu-id="7b8c9-139">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="7b8c9-140">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="7b8c9-140">Return Value - changedDate</span></span>

<span data-ttu-id="7b8c9-141">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-141">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="7b8c9-142">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="7b8c9-142">Method changedTime</span></span>

<span data-ttu-id="7b8c9-143">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-143">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="7b8c9-144">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="7b8c9-144">Parameters - changedTime</span></span>

<span data-ttu-id="7b8c9-145">値</span><span class="sxs-lookup"><span data-stu-id="7b8c9-145">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="7b8c9-146">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="7b8c9-146">Return Value - changedTime</span></span>

<span data-ttu-id="7b8c9-147">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-147">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="7b8c9-148">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="7b8c9-148">Method createdBy</span></span>

<span data-ttu-id="7b8c9-149">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-149">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="7b8c9-150">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="7b8c9-150">Parameters - createdBy</span></span>

<span data-ttu-id="7b8c9-151">値</span><span class="sxs-lookup"><span data-stu-id="7b8c9-151">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="7b8c9-152">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="7b8c9-152">Return Value - createdBy</span></span>

<span data-ttu-id="7b8c9-153">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-153">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="7b8c9-154">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="7b8c9-154">Method creationDate</span></span>

<span data-ttu-id="7b8c9-155">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-155">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="7b8c9-156">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="7b8c9-156">Parameters - creationDate</span></span>

<span data-ttu-id="7b8c9-157">値</span><span class="sxs-lookup"><span data-stu-id="7b8c9-157">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="7b8c9-158">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="7b8c9-158">Return Value - creationDate</span></span>

<span data-ttu-id="7b8c9-159">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-159">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="7b8c9-160">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="7b8c9-160">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="7b8c9-161">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="7b8c9-161">Parameters - creationTime</span></span>

<span data-ttu-id="7b8c9-162">値</span><span class="sxs-lookup"><span data-stu-id="7b8c9-162">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="7b8c9-163">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="7b8c9-163">Return Value - creationTime</span></span>

## <a name="method-helptext"></a><span data-ttu-id="7b8c9-164">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="7b8c9-164">Method helpText</span></span>

<span data-ttu-id="7b8c9-165">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-165">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="7b8c9-166">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="7b8c9-166">Parameters - helpText</span></span>

<span data-ttu-id="7b8c9-167">値</span><span class="sxs-lookup"><span data-stu-id="7b8c9-167">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="7b8c9-168">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="7b8c9-168">Return Value - helpText</span></span>

<span data-ttu-id="7b8c9-169">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-169">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="7b8c9-170">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="7b8c9-170">Remarks - helpText</span></span>

<span data-ttu-id="7b8c9-171">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-171">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="7b8c9-172">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-172">The help text must not exceed 250 characters.</span></span>

## <a name="method-label"></a><span data-ttu-id="7b8c9-173">メソッド label</span><span class="sxs-lookup"><span data-stu-id="7b8c9-173">Method label</span></span>

<span data-ttu-id="7b8c9-174">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-174">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="7b8c9-175">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="7b8c9-175">Parameters - label</span></span>

<span data-ttu-id="7b8c9-176">値</span><span class="sxs-lookup"><span data-stu-id="7b8c9-176">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="7b8c9-177">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="7b8c9-177">Return Value - label</span></span>

<span data-ttu-id="7b8c9-178">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-178">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="7b8c9-179">備考 - label</span><span class="sxs-lookup"><span data-stu-id="7b8c9-179">Remarks - label</span></span>

<span data-ttu-id="7b8c9-180">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-180">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="7b8c9-181">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-181">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-name"></a><span data-ttu-id="7b8c9-182">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7b8c9-182">Method name</span></span>

<span data-ttu-id="7b8c9-183">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-183">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="7b8c9-184">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="7b8c9-184">Parameters - name</span></span>

<span data-ttu-id="7b8c9-185">値</span><span class="sxs-lookup"><span data-stu-id="7b8c9-185">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="7b8c9-186">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="7b8c9-186">Return Value - name</span></span>

<span data-ttu-id="7b8c9-187">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-187">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="7b8c9-188">備考 - name</span><span class="sxs-lookup"><span data-stu-id="7b8c9-188">Remarks - name</span></span>

<span data-ttu-id="7b8c9-189">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-189">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7b8c9-190">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-190">Begins with a letter.</span></span>
-   <span data-ttu-id="7b8c9-191">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-191">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="7b8c9-192">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-192">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="7b8c9-193">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-193">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7b8c9-194">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7b8c9-194">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-origin"></a><span data-ttu-id="7b8c9-195">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="7b8c9-195">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="7b8c9-196">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="7b8c9-196">Parameters - origin</span></span>

<span data-ttu-id="7b8c9-197">値</span><span class="sxs-lookup"><span data-stu-id="7b8c9-197">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="7b8c9-198">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="7b8c9-198">Return Value - origin</span></span>

## <a name="method-createwebmenufunction"></a><span data-ttu-id="7b8c9-199">メソッド createWebMenuFunction</span><span class="sxs-lookup"><span data-stu-id="7b8c9-199">Method createWebMenuFunction</span></span>

```xpp
public static WebMenuFunction createWebMenuFunction(str name, WebMenuItemType webMenuItemType)
```

### <a name="parameters---createwebmenufunction"></a><span data-ttu-id="7b8c9-200">パラメーター - createWebMenuFunction</span><span class="sxs-lookup"><span data-stu-id="7b8c9-200">Parameters - createWebMenuFunction</span></span>

<span data-ttu-id="7b8c9-201">名前</span><span class="sxs-lookup"><span data-stu-id="7b8c9-201">name</span></span>  

<!-- -->

<span data-ttu-id="7b8c9-202">webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="7b8c9-202">webMenuItemType</span></span>  

### <a name="return-value---createwebmenufunction"></a><span data-ttu-id="7b8c9-203">戻り値 - createWebMenuFunction</span><span class="sxs-lookup"><span data-stu-id="7b8c9-203">Return Value - createWebMenuFunction</span></span>

