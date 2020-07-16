---
title: WebletItem クラス
description: このトピックでは、WebletItem クラスについて説明します。
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
ms.openlocfilehash: ee947cb8b647781c2805c643e6e90ec5f681a04c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502686"
---
# <a name="class-webletitem"></a><span data-ttu-id="7948e-103">クラス WebletItem</span><span class="sxs-lookup"><span data-stu-id="7948e-103">Class WebletItem</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class WebletItem extends SecureNode
```

<span data-ttu-id="7948e-104">WebletItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7948e-104">The WebletItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="7948e-105">備考</span><span class="sxs-lookup"><span data-stu-id="7948e-105">Remarks</span></span>

<span data-ttu-id="7948e-106">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7948e-106">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="7948e-107">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7948e-107">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

## <a name="examples"></a><span data-ttu-id="7948e-108">例</span><span class="sxs-lookup"><span data-stu-id="7948e-108">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="7948e-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="7948e-109">Methods</span></span>

| <span data-ttu-id="7948e-110">方法</span><span class="sxs-lookup"><span data-stu-id="7948e-110">Method</span></span>                                            | <span data-ttu-id="7948e-111">説明</span><span class="sxs-lookup"><span data-stu-id="7948e-111">Description</span></span>                                                                                                                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7948e-112">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-112">public str changedBy(\[str value\])</span></span>               | <span data-ttu-id="7948e-113">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-113">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="7948e-114">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-114">public Date changedDate(\[Date value\])</span></span>           | <span data-ttu-id="7948e-115">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-115">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="7948e-116">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-116">public str changedTime(\[str value\])</span></span>             | <span data-ttu-id="7948e-117">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-117">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="7948e-118">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-118">public str createdBy(\[str value\])</span></span>               | <span data-ttu-id="7948e-119">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-119">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="7948e-120">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-120">public Date creationDate(\[Date value\])</span></span>          | <span data-ttu-id="7948e-121">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-121">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="7948e-122">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-122">public str creationTime(\[str value\])</span></span>            |                                                                                                                                               |
| <span data-ttu-id="7948e-123">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-123">public int enumParameter(\[int value\])</span></span>           | <span data-ttu-id="7948e-124">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-124">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>                                   |
| <span data-ttu-id="7948e-125">public EnumId enumTypeParameter(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-125">public EnumId enumTypeParameter(\[EnumId value\])</span></span> | <span data-ttu-id="7948e-126">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-126">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                                                       |
| <span data-ttu-id="7948e-127">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-127">public str helpText(\[str value\])</span></span>                | <span data-ttu-id="7948e-128">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-128">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="7948e-129">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-129">public str label(\[str value\])</span></span>                   | <span data-ttu-id="7948e-130">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-130">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="7948e-131">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-131">public str name(\[str value\])</span></span>                    | <span data-ttu-id="7948e-132">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-132">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="7948e-133">public str object(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-133">public str object(\[str value\])</span></span>                  | <span data-ttu-id="7948e-134">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-134">Gets or sets the object that the MenuFunction class runs.</span></span>                                                                                     |
| <span data-ttu-id="7948e-135">public int objectType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-135">public int objectType(\[int value\])</span></span>              |                                                                                                                                               |
| <span data-ttu-id="7948e-136">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-136">public Guid origin(\[Guid value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="7948e-137">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-137">public str parameters(\[str value\])</span></span>              | <span data-ttu-id="7948e-138">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-138">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                        |
| <span data-ttu-id="7948e-139">public str reportDesign(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7948e-139">public str reportDesign(\[str value\])</span></span>            |                                                                                                                                               |
| <span data-ttu-id="7948e-140">public void new(str name)</span><span class="sxs-lookup"><span data-stu-id="7948e-140">public void new(str name)</span></span>                         | <span data-ttu-id="7948e-141">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="7948e-141">Microsoft internal use only.</span></span>                                                                                                                  |

## <a name="method-changedby"></a><span data-ttu-id="7948e-142">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="7948e-142">Method changedBy</span></span>

<span data-ttu-id="7948e-143">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-143">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="7948e-144">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="7948e-144">Parameters - changedBy</span></span>

<span data-ttu-id="7948e-145">値</span><span class="sxs-lookup"><span data-stu-id="7948e-145">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="7948e-146">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="7948e-146">Return Value - changedBy</span></span>

<span data-ttu-id="7948e-147">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7948e-147">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="7948e-148">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="7948e-148">Method changedDate</span></span>

<span data-ttu-id="7948e-149">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-149">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="7948e-150">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="7948e-150">Parameters - changedDate</span></span>

<span data-ttu-id="7948e-151">値</span><span class="sxs-lookup"><span data-stu-id="7948e-151">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="7948e-152">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="7948e-152">Return Value - changedDate</span></span>

<span data-ttu-id="7948e-153">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="7948e-153">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="7948e-154">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="7948e-154">Method changedTime</span></span>

<span data-ttu-id="7948e-155">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-155">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="7948e-156">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="7948e-156">Parameters - changedTime</span></span>

<span data-ttu-id="7948e-157">値</span><span class="sxs-lookup"><span data-stu-id="7948e-157">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="7948e-158">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="7948e-158">Return Value - changedTime</span></span>

<span data-ttu-id="7948e-159">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="7948e-159">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="7948e-160">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="7948e-160">Method createdBy</span></span>

<span data-ttu-id="7948e-161">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-161">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="7948e-162">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="7948e-162">Parameters - createdBy</span></span>

<span data-ttu-id="7948e-163">値</span><span class="sxs-lookup"><span data-stu-id="7948e-163">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="7948e-164">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="7948e-164">Return Value - createdBy</span></span>

<span data-ttu-id="7948e-165">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="7948e-165">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="7948e-166">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="7948e-166">Method creationDate</span></span>

<span data-ttu-id="7948e-167">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-167">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="7948e-168">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="7948e-168">Parameters - creationDate</span></span>

<span data-ttu-id="7948e-169">値</span><span class="sxs-lookup"><span data-stu-id="7948e-169">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="7948e-170">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="7948e-170">Return Value - creationDate</span></span>

<span data-ttu-id="7948e-171">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="7948e-171">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="7948e-172">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="7948e-172">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="7948e-173">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="7948e-173">Parameters - creationTime</span></span>

<span data-ttu-id="7948e-174">値</span><span class="sxs-lookup"><span data-stu-id="7948e-174">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="7948e-175">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="7948e-175">Return Value - creationTime</span></span>

## <a name="method-enumparameter"></a><span data-ttu-id="7948e-176">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="7948e-176">Method enumParameter</span></span>

<span data-ttu-id="7948e-177">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-177">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

```xpp
public int enumParameter([int value])
```

### <a name="parameters---enumparameter"></a><span data-ttu-id="7948e-178">パラメーター - enumParameter</span><span class="sxs-lookup"><span data-stu-id="7948e-178">Parameters - enumParameter</span></span>

<span data-ttu-id="7948e-179">値</span><span class="sxs-lookup"><span data-stu-id="7948e-179">value</span></span>  

### <a name="return-value---enumparameter"></a><span data-ttu-id="7948e-180">戻り値 - enumParameter</span><span class="sxs-lookup"><span data-stu-id="7948e-180">Return Value - enumParameter</span></span>

<span data-ttu-id="7948e-181">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="7948e-181">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

## <a name="method-enumtypeparameter"></a><span data-ttu-id="7948e-182">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="7948e-182">Method enumTypeParameter</span></span>

<span data-ttu-id="7948e-183">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-183">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

```xpp
public EnumId enumTypeParameter([EnumId value])
```

### <a name="parameters---enumtypeparameter"></a><span data-ttu-id="7948e-184">パラメーター - enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="7948e-184">Parameters - enumTypeParameter</span></span>

<span data-ttu-id="7948e-185">値</span><span class="sxs-lookup"><span data-stu-id="7948e-185">value</span></span>  

### <a name="return-value---enumtypeparameter"></a><span data-ttu-id="7948e-186">戻り値 - enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="7948e-186">Return Value - enumTypeParameter</span></span>

<span data-ttu-id="7948e-187">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="7948e-187">The enumTypeParameter property for the MenuFunction class.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="7948e-188">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="7948e-188">Method helpText</span></span>

<span data-ttu-id="7948e-189">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-189">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="7948e-190">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="7948e-190">Parameters - helpText</span></span>

<span data-ttu-id="7948e-191">値</span><span class="sxs-lookup"><span data-stu-id="7948e-191">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="7948e-192">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="7948e-192">Return Value - helpText</span></span>

<span data-ttu-id="7948e-193">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="7948e-193">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="7948e-194">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="7948e-194">Remarks - helpText</span></span>

<span data-ttu-id="7948e-195">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-195">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="7948e-196">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="7948e-196">The help text must not exceed 250 characters.</span></span>

## <a name="method-label"></a><span data-ttu-id="7948e-197">メソッド label</span><span class="sxs-lookup"><span data-stu-id="7948e-197">Method label</span></span>

<span data-ttu-id="7948e-198">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-198">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="7948e-199">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="7948e-199">Parameters - label</span></span>

<span data-ttu-id="7948e-200">値</span><span class="sxs-lookup"><span data-stu-id="7948e-200">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="7948e-201">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="7948e-201">Return Value - label</span></span>

<span data-ttu-id="7948e-202">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="7948e-202">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="7948e-203">備考 - label</span><span class="sxs-lookup"><span data-stu-id="7948e-203">Remarks - label</span></span>

<span data-ttu-id="7948e-204">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-204">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="7948e-205">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="7948e-205">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-name"></a><span data-ttu-id="7948e-206">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7948e-206">Method name</span></span>

<span data-ttu-id="7948e-207">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-207">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="7948e-208">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="7948e-208">Parameters - name</span></span>

<span data-ttu-id="7948e-209">値</span><span class="sxs-lookup"><span data-stu-id="7948e-209">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="7948e-210">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="7948e-210">Return Value - name</span></span>

<span data-ttu-id="7948e-211">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7948e-211">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="7948e-212">備考 - name</span><span class="sxs-lookup"><span data-stu-id="7948e-212">Remarks - name</span></span>

<span data-ttu-id="7948e-213">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7948e-213">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7948e-214">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="7948e-214">Begins with a letter.</span></span>
-   <span data-ttu-id="7948e-215">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="7948e-215">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="7948e-216">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7948e-216">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="7948e-217">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7948e-217">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7948e-218">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7948e-218">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, classes, and so on.</span></span>

## <a name="method-object"></a><span data-ttu-id="7948e-219">メソッド object</span><span class="sxs-lookup"><span data-stu-id="7948e-219">Method object</span></span>

<span data-ttu-id="7948e-220">MenuFunction クラスが実行するオブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-220">Gets or sets the object that the MenuFunction class runs.</span></span>

```xpp
public str object([str value])
```

### <a name="parameters---object"></a><span data-ttu-id="7948e-221">パラメーター - object</span><span class="sxs-lookup"><span data-stu-id="7948e-221">Parameters - object</span></span>

<span data-ttu-id="7948e-222">値</span><span class="sxs-lookup"><span data-stu-id="7948e-222">value</span></span>  

### <a name="return-value---object"></a><span data-ttu-id="7948e-223">戻り値 - object</span><span class="sxs-lookup"><span data-stu-id="7948e-223">Return Value - object</span></span>

<span data-ttu-id="7948e-224">MenuFunction クラスが実行するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="7948e-224">The object that the MenuFunction class runs.</span></span>

### <a name="remarks---object"></a><span data-ttu-id="7948e-225">備考 - object</span><span class="sxs-lookup"><span data-stu-id="7948e-225">Remarks - object</span></span>

<span data-ttu-id="7948e-226">プロパティ値は、次のオブジェクトのいずれかである場合があります。</span><span class="sxs-lookup"><span data-stu-id="7948e-226">property value may be one of the following objects:</span></span>

-   <span data-ttu-id="7948e-227">フォーム。</span><span class="sxs-lookup"><span data-stu-id="7948e-227">Form.</span></span>
-   <span data-ttu-id="7948e-228">レポート。</span><span class="sxs-lookup"><span data-stu-id="7948e-228">Report.</span></span>
-   <span data-ttu-id="7948e-229">ジョブ。</span><span class="sxs-lookup"><span data-stu-id="7948e-229">Job.</span></span>
-   <span data-ttu-id="7948e-230">クラス。</span><span class="sxs-lookup"><span data-stu-id="7948e-230">Class.</span></span>
-   <span data-ttu-id="7948e-231">クエリ。</span><span class="sxs-lookup"><span data-stu-id="7948e-231">Query.</span></span>

## <a name="method-objecttype"></a><span data-ttu-id="7948e-232">メソッド objectType</span><span class="sxs-lookup"><span data-stu-id="7948e-232">Method objectType</span></span>

```xpp
public int objectType([int value])
```

### <a name="parameters---objecttype"></a><span data-ttu-id="7948e-233">パラメーター - objectType</span><span class="sxs-lookup"><span data-stu-id="7948e-233">Parameters - objectType</span></span>

<span data-ttu-id="7948e-234">値</span><span class="sxs-lookup"><span data-stu-id="7948e-234">value</span></span>  

### <a name="return-value---objecttype"></a><span data-ttu-id="7948e-235">戻り値 - objectType</span><span class="sxs-lookup"><span data-stu-id="7948e-235">Return Value - objectType</span></span>

## <a name="method-origin"></a><span data-ttu-id="7948e-236">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="7948e-236">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="7948e-237">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="7948e-237">Parameters - origin</span></span>

<span data-ttu-id="7948e-238">値</span><span class="sxs-lookup"><span data-stu-id="7948e-238">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="7948e-239">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="7948e-239">Return Value - origin</span></span>

## <a name="method-parameters"></a><span data-ttu-id="7948e-240">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="7948e-240">Method parameters</span></span>

<span data-ttu-id="7948e-241">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7948e-241">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="7948e-242">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="7948e-242">Parameters - parameters</span></span>

<span data-ttu-id="7948e-243">値</span><span class="sxs-lookup"><span data-stu-id="7948e-243">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="7948e-244">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="7948e-244">Return Value - parameters</span></span>

<span data-ttu-id="7948e-245">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="7948e-245">The list of parameters that are passed to the object.</span></span>

### <a name="remarks---parameters"></a><span data-ttu-id="7948e-246">備考 - parameters</span><span class="sxs-lookup"><span data-stu-id="7948e-246">Remarks - parameters</span></span>

<span data-ttu-id="7948e-247">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="7948e-247">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="7948e-248">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="7948e-248">Objects ignore passed, unrecognized parameters.</span></span>

## <a name="method-reportdesign"></a><span data-ttu-id="7948e-249">メソッド reportDesign</span><span class="sxs-lookup"><span data-stu-id="7948e-249">Method reportDesign</span></span>

```xpp
public str reportDesign([str value])
```

### <a name="parameters---reportdesign"></a><span data-ttu-id="7948e-250">パラメーター - reportDesign</span><span class="sxs-lookup"><span data-stu-id="7948e-250">Parameters - reportDesign</span></span>

<span data-ttu-id="7948e-251">値</span><span class="sxs-lookup"><span data-stu-id="7948e-251">value</span></span>  

### <a name="return-value---reportdesign"></a><span data-ttu-id="7948e-252">戻り値 - reportDesign</span><span class="sxs-lookup"><span data-stu-id="7948e-252">Return Value - reportDesign</span></span>

## <a name="method-new"></a><span data-ttu-id="7948e-253">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7948e-253">Method new</span></span>

<span data-ttu-id="7948e-254">Microsoft 社内のみで使用。</span><span class="sxs-lookup"><span data-stu-id="7948e-254">Microsoft internal use only.</span></span>

```xpp
public void new(str name)
```

### <a name="parameters---new"></a><span data-ttu-id="7948e-255">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="7948e-255">Parameters - new</span></span>

<span data-ttu-id="7948e-256">名前</span><span class="sxs-lookup"><span data-stu-id="7948e-256">name</span></span>  

