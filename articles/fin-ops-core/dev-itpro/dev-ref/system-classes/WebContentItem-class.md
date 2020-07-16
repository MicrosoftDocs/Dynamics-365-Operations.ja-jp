---
title: WebContentItem クラス
description: このトピックでは、WebContentItem クラスについて説明します。
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
ms.openlocfilehash: e590b6351bfbab09a2b590118cdbaf2184e6fc76
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502775"
---
# <a name="class-webcontentitem"></a><span data-ttu-id="87b8f-103">クラス WebContentItem</span><span class="sxs-lookup"><span data-stu-id="87b8f-103">Class WebContentItem</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class WebContentItem extends SecureNode
```

<span data-ttu-id="87b8f-104">WebContentItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="87b8f-104">The WebContentItem class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="87b8f-105">備考</span><span class="sxs-lookup"><span data-stu-id="87b8f-105">Remarks</span></span>

<span data-ttu-id="87b8f-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="87b8f-107">例</span><span class="sxs-lookup"><span data-stu-id="87b8f-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="87b8f-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="87b8f-108">Methods</span></span>

| <span data-ttu-id="87b8f-109">方法</span><span class="sxs-lookup"><span data-stu-id="87b8f-109">Method</span></span>                                            | <span data-ttu-id="87b8f-110">説明</span><span class="sxs-lookup"><span data-stu-id="87b8f-110">Description</span></span>                                                                                                                               |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87b8f-111">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-111">public str changedBy(\[str value\])</span></span>               | <span data-ttu-id="87b8f-112">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-112">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="87b8f-113">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-113">public Date changedDate(\[Date value\])</span></span>           | <span data-ttu-id="87b8f-114">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-114">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="87b8f-115">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-115">public str changedTime(\[str value\])</span></span>             | <span data-ttu-id="87b8f-116">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-116">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="87b8f-117">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-117">public str createdBy(\[str value\])</span></span>               | <span data-ttu-id="87b8f-118">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-118">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="87b8f-119">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-119">public Date creationDate(\[Date value\])</span></span>          | <span data-ttu-id="87b8f-120">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-120">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="87b8f-121">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-121">public str creationTime(\[str value\])</span></span>            |                                                                                                                                           |
| <span data-ttu-id="87b8f-122">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-122">public int enumParameter(\[int value\])</span></span>           | <span data-ttu-id="87b8f-123">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-123">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>                               |
| <span data-ttu-id="87b8f-124">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-124">public EnumId enumTypeParameter(\[EnumId value\])</span></span> | <span data-ttu-id="87b8f-125">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-125">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                                                   |
| <span data-ttu-id="87b8f-126">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-126">public str helpText(\[str value\])</span></span>                | <span data-ttu-id="87b8f-127">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-127">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="87b8f-128">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-128">public str label(\[str value\])</span></span>                   | <span data-ttu-id="87b8f-129">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-129">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="87b8f-130">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-130">public str name(\[str value\])</span></span>                    | <span data-ttu-id="87b8f-131">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-131">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="87b8f-132">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-132">public str object(\[str value\])</span></span>                  | <span data-ttu-id="87b8f-133">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-133">Gets or sets the object that the MenuFunction class runs.</span></span>                                                                                 |
| <span data-ttu-id="87b8f-134">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-134">public int objectType(\[int value\])</span></span>              |                                                                                                                                           |
| <span data-ttu-id="87b8f-135">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-135">public Guid origin(\[Guid value\])</span></span>                |                                                                                                                                           |
| <span data-ttu-id="87b8f-136">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-136">public str parameters(\[str value\])</span></span>              | <span data-ttu-id="87b8f-137">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-137">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                    |
| <span data-ttu-id="87b8f-138">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="87b8f-138">public str reportDesign(\[str value\])</span></span>            |                                                                                                                                           |

## <a name="method-changedby"></a><span data-ttu-id="87b8f-139">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="87b8f-139">Method changedBy</span></span>

<span data-ttu-id="87b8f-140">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-140">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="87b8f-141">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="87b8f-141">Parameters - changedBy</span></span>

<span data-ttu-id="87b8f-142">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-142">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="87b8f-143">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="87b8f-143">Return Value - changedBy</span></span>

<span data-ttu-id="87b8f-144">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="87b8f-144">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="87b8f-145">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="87b8f-145">Method changedDate</span></span>

<span data-ttu-id="87b8f-146">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-146">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="87b8f-147">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="87b8f-147">Parameters - changedDate</span></span>

<span data-ttu-id="87b8f-148">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-148">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="87b8f-149">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="87b8f-149">Return Value - changedDate</span></span>

<span data-ttu-id="87b8f-150">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="87b8f-150">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="87b8f-151">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="87b8f-151">Method changedTime</span></span>

<span data-ttu-id="87b8f-152">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-152">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="87b8f-153">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="87b8f-153">Parameters - changedTime</span></span>

<span data-ttu-id="87b8f-154">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-154">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="87b8f-155">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="87b8f-155">Return Value - changedTime</span></span>

<span data-ttu-id="87b8f-156">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="87b8f-156">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="87b8f-157">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="87b8f-157">Method createdBy</span></span>

<span data-ttu-id="87b8f-158">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-158">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="87b8f-159">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="87b8f-159">Parameters - createdBy</span></span>

<span data-ttu-id="87b8f-160">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-160">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="87b8f-161">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="87b8f-161">Return Value - createdBy</span></span>

<span data-ttu-id="87b8f-162">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="87b8f-162">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="87b8f-163">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="87b8f-163">Method creationDate</span></span>

<span data-ttu-id="87b8f-164">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-164">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="87b8f-165">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="87b8f-165">Parameters - creationDate</span></span>

<span data-ttu-id="87b8f-166">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-166">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="87b8f-167">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="87b8f-167">Return Value - creationDate</span></span>

<span data-ttu-id="87b8f-168">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="87b8f-168">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="87b8f-169">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="87b8f-169">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="87b8f-170">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="87b8f-170">Parameters - creationTime</span></span>

<span data-ttu-id="87b8f-171">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-171">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="87b8f-172">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="87b8f-172">Return Value - creationTime</span></span>

## <a name="method-enumparameter"></a><span data-ttu-id="87b8f-173">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="87b8f-173">Method enumParameter</span></span>

<span data-ttu-id="87b8f-174">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-174">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

```xpp
public int enumParameter([int value])
```

### <a name="parameters---enumparameter"></a><span data-ttu-id="87b8f-175">パラメーター - enumParameter</span><span class="sxs-lookup"><span data-stu-id="87b8f-175">Parameters - enumParameter</span></span>

<span data-ttu-id="87b8f-176">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-176">value</span></span>  

### <a name="return-value---enumparameter"></a><span data-ttu-id="87b8f-177">戻り値 - enumParameter</span><span class="sxs-lookup"><span data-stu-id="87b8f-177">Return Value - enumParameter</span></span>

<span data-ttu-id="87b8f-178">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="87b8f-178">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

## <a name="method-enumtypeparameter"></a><span data-ttu-id="87b8f-179">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="87b8f-179">Method enumTypeParameter</span></span>

<span data-ttu-id="87b8f-180">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-180">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

```xpp
public EnumId enumTypeParameter([EnumId value])
```

### <a name="parameters---enumtypeparameter"></a><span data-ttu-id="87b8f-181">パラメーター - enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="87b8f-181">Parameters - enumTypeParameter</span></span>

<span data-ttu-id="87b8f-182">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-182">value</span></span>  

### <a name="return-value---enumtypeparameter"></a><span data-ttu-id="87b8f-183">戻り値 - enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="87b8f-183">Return Value - enumTypeParameter</span></span>

<span data-ttu-id="87b8f-184">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="87b8f-184">The enumTypeParameter property for the MenuFunction class.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="87b8f-185">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="87b8f-185">Method helpText</span></span>

<span data-ttu-id="87b8f-186">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-186">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="87b8f-187">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="87b8f-187">Parameters - helpText</span></span>

<span data-ttu-id="87b8f-188">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-188">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="87b8f-189">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="87b8f-189">Return Value - helpText</span></span>

<span data-ttu-id="87b8f-190">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="87b8f-190">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="87b8f-191">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="87b8f-191">Remarks - helpText</span></span>

<span data-ttu-id="87b8f-192">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-192">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="87b8f-193">ダイアログ ボックス。</span><span class="sxs-lookup"><span data-stu-id="87b8f-193">dialog box.</span></span> <span data-ttu-id="87b8f-194">ヘルプ テキストは、250文字以下である必要があります。</span><span class="sxs-lookup"><span data-stu-id="87b8f-194">The The help text must not exceed 250 characters.</span></span>

## <a name="method-label"></a><span data-ttu-id="87b8f-195">メソッド label</span><span class="sxs-lookup"><span data-stu-id="87b8f-195">Method label</span></span>

<span data-ttu-id="87b8f-196">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-196">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="87b8f-197">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="87b8f-197">Parameters - label</span></span>

<span data-ttu-id="87b8f-198">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-198">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="87b8f-199">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="87b8f-199">Return Value - label</span></span>

<span data-ttu-id="87b8f-200">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="87b8f-200">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="87b8f-201">備考 - label</span><span class="sxs-lookup"><span data-stu-id="87b8f-201">Remarks - label</span></span>

<span data-ttu-id="87b8f-202">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-202">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="87b8f-203">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="87b8f-203">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-name"></a><span data-ttu-id="87b8f-204">メソッド名</span><span class="sxs-lookup"><span data-stu-id="87b8f-204">Method name</span></span>

<span data-ttu-id="87b8f-205">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-205">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="87b8f-206">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="87b8f-206">Parameters - name</span></span>

<span data-ttu-id="87b8f-207">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-207">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="87b8f-208">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="87b8f-208">Return Value - name</span></span>

<span data-ttu-id="87b8f-209">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="87b8f-209">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="87b8f-210">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="87b8f-210">Remarks - name</span></span>

<span data-ttu-id="87b8f-211">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="87b8f-211">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="87b8f-212">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="87b8f-212">Begins with a letter.</span></span>
-   <span data-ttu-id="87b8f-213">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="87b8f-213">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="87b8f-214">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="87b8f-214">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="87b8f-215">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="87b8f-215">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="87b8f-216">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="87b8f-216">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-object"></a><span data-ttu-id="87b8f-217">メソッド object</span><span class="sxs-lookup"><span data-stu-id="87b8f-217">Method object</span></span>

<span data-ttu-id="87b8f-218">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-218">Gets or sets the object that the MenuFunction class runs.</span></span>

```xpp
public str object([str value])
```

### <a name="parameters---object"></a><span data-ttu-id="87b8f-219">パラメーター - object</span><span class="sxs-lookup"><span data-stu-id="87b8f-219">Parameters - object</span></span>

<span data-ttu-id="87b8f-220">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-220">value</span></span>  

### <a name="return-value---object"></a><span data-ttu-id="87b8f-221">戻り値 - object</span><span class="sxs-lookup"><span data-stu-id="87b8f-221">Return Value - object</span></span>

<span data-ttu-id="87b8f-222">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="87b8f-222">The object that the MenuFunction class runs.</span></span>

### <a name="remarks---object"></a><span data-ttu-id="87b8f-223">備考 - object</span><span class="sxs-lookup"><span data-stu-id="87b8f-223">Remarks - object</span></span>

<span data-ttu-id="87b8f-224">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="87b8f-224">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="87b8f-225">フォーム</span><span class="sxs-lookup"><span data-stu-id="87b8f-225">Form</span></span>
-   <span data-ttu-id="87b8f-226">報告</span><span class="sxs-lookup"><span data-stu-id="87b8f-226">Report</span></span>
-   <span data-ttu-id="87b8f-227">ジョブ</span><span class="sxs-lookup"><span data-stu-id="87b8f-227">Job</span></span>
-   <span data-ttu-id="87b8f-228">クラス</span><span class="sxs-lookup"><span data-stu-id="87b8f-228">Class</span></span>
-   <span data-ttu-id="87b8f-229">クエリ</span><span class="sxs-lookup"><span data-stu-id="87b8f-229">Query</span></span>

## <a name="method-objecttype"></a><span data-ttu-id="87b8f-230">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="87b8f-230">Method objectType</span></span>

```xpp
public int objectType([int value])
```

### <a name="parameters---objecttype"></a><span data-ttu-id="87b8f-231">パラメーター - objectType</span><span class="sxs-lookup"><span data-stu-id="87b8f-231">Parameters - objectType</span></span>

<span data-ttu-id="87b8f-232">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-232">value</span></span>  

### <a name="return-value---objecttype"></a><span data-ttu-id="87b8f-233">戻り値 - objectType</span><span class="sxs-lookup"><span data-stu-id="87b8f-233">Return Value - objectType</span></span>

## <a name="method-origin"></a><span data-ttu-id="87b8f-234">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="87b8f-234">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="87b8f-235">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="87b8f-235">Parameters - origin</span></span>

<span data-ttu-id="87b8f-236">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-236">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="87b8f-237">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="87b8f-237">Return Value - origin</span></span>

## <a name="method-parameters"></a><span data-ttu-id="87b8f-238">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="87b8f-238">Method parameters</span></span>

<span data-ttu-id="87b8f-239">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-239">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="87b8f-240">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="87b8f-240">Parameters - parameters</span></span>

<span data-ttu-id="87b8f-241">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-241">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="87b8f-242">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="87b8f-242">Return Value - parameters</span></span>

<span data-ttu-id="87b8f-243">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="87b8f-243">The list of parameters that are passed to the object.</span></span>

### <a name="remarks---parameters"></a><span data-ttu-id="87b8f-244">備考 - parameters</span><span class="sxs-lookup"><span data-stu-id="87b8f-244">Remarks - parameters</span></span>

<span data-ttu-id="87b8f-245">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="87b8f-245">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="87b8f-246">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="87b8f-246">Objects ignore passed, unrecognized parameters.</span></span>

## <a name="method-reportdesign"></a><span data-ttu-id="87b8f-247">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="87b8f-247">Method reportDesign</span></span>

```xpp
public str reportDesign([str value])
```

### <a name="parameters---reportdesign"></a><span data-ttu-id="87b8f-248">パラメーター - reportDesign</span><span class="sxs-lookup"><span data-stu-id="87b8f-248">Parameters - reportDesign</span></span>

<span data-ttu-id="87b8f-249">値</span><span class="sxs-lookup"><span data-stu-id="87b8f-249">value</span></span>  

### <a name="return-value---reportdesign"></a><span data-ttu-id="87b8f-250">戻り値 - reportDesign</span><span class="sxs-lookup"><span data-stu-id="87b8f-250">Return Value - reportDesign</span></span>

