---
title: WebMenu クラス
description: このトピックでは、WebMenu クラスについて説明します。
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
ms.openlocfilehash: b4bb194e176a806723891d8ded07513e6a1e7c2e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503004"
---
# <a name="class-webmenu"></a><span data-ttu-id="de114-103">クラス WebMenu</span><span class="sxs-lookup"><span data-stu-id="de114-103">Class WebMenu</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class WebMenu extends TreeNode
```

<span data-ttu-id="de114-104">WebMenu クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="de114-104">The WebMenu class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="de114-105">備考</span><span class="sxs-lookup"><span data-stu-id="de114-105">Remarks</span></span>

<span data-ttu-id="de114-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="de114-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="de114-107">例</span><span class="sxs-lookup"><span data-stu-id="de114-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="de114-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="de114-108">Methods</span></span>

| <span data-ttu-id="de114-109">方法</span><span class="sxs-lookup"><span data-stu-id="de114-109">Method</span></span>                                                                   | <span data-ttu-id="de114-110">説明</span><span class="sxs-lookup"><span data-stu-id="de114-110">Description</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de114-111">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de114-111">public str changedBy(\[str value\])</span></span>                                      | <span data-ttu-id="de114-112">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-112">Gets or sets the name of the user who last changed the application object.</span></span>                                                                    |
| <span data-ttu-id="de114-113">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="de114-113">public Date changedDate(\[Date value\])</span></span>                                  | <span data-ttu-id="de114-114">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-114">Gets or sets the date an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="de114-115">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de114-115">public str changedTime(\[str value\])</span></span>                                    | <span data-ttu-id="de114-116">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-116">Gets or sets the time an application object was last changed.</span></span>                                                                                 |
| <span data-ttu-id="de114-117">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="de114-117">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="de114-118">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-118">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                           |
| <span data-ttu-id="de114-119">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de114-119">public str createdBy(\[str value\])</span></span>                                      | <span data-ttu-id="de114-120">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-120">Gets or sets the name of the user who created the application object.</span></span>                                                                         |
| <span data-ttu-id="de114-121">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="de114-121">public Date creationDate(\[Date value\])</span></span>                                 | <span data-ttu-id="de114-122">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-122">Gets or sets the date an application object was created.</span></span>                                                                                      |
| <span data-ttu-id="de114-123">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de114-123">public str creationTime(\[str value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="de114-124">public boolean highlightSelected(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de114-124">public boolean highlightSelected(\[boolean value\])</span></span>                      |                                                                                                                                               |
| <span data-ttu-id="de114-125">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de114-125">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="de114-126">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-126">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="de114-127">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de114-127">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="de114-128">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="de114-128">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span>           |                                                                                                                                               |
| <span data-ttu-id="de114-129">public str menuName()</span><span class="sxs-lookup"><span data-stu-id="de114-129">public str menuName()</span></span>                                                    |                                                                                                                                               |
| <span data-ttu-id="de114-130">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de114-130">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="de114-131">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-131">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="de114-132">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="de114-132">public int neededAccessLevel(\[int value\])</span></span>                              | <span data-ttu-id="de114-133">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-133">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>                                                                       |
| <span data-ttu-id="de114-134">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="de114-134">public Guid origin(\[Guid value\])</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="de114-135">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="de114-135">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="de114-136">public boolean setCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de114-136">public boolean setCompany(\[boolean value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="de114-137">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="de114-137">public boolean showParentModule(\[boolean value\])</span></span>                       |                                                                                                                                               |
| <span data-ttu-id="de114-138">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="de114-138">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="de114-139">public void addSeparator()</span><span class="sxs-lookup"><span data-stu-id="de114-139">public void addSeparator()</span></span>                                               |                                                                                                                                               |
| <span data-ttu-id="de114-140">public void makeMenu(Object outputClass)</span><span class="sxs-lookup"><span data-stu-id="de114-140">public void makeMenu(Object outputClass)</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="de114-141">public void addSubmenu(str name)</span><span class="sxs-lookup"><span data-stu-id="de114-141">public void addSubmenu(str name)</span></span>                                         |                                                                                                                                               |
| <span data-ttu-id="de114-142">public void new(str Name)</span><span class="sxs-lookup"><span data-stu-id="de114-142">public void new(str Name)</span></span>                                                | <span data-ttu-id="de114-143">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="de114-143">Initializes a new instance of the TreeNode class.</span></span>                                                                                             |
| <span data-ttu-id="de114-144">public void addMenuitem(WebMenuFunction webMenuFunction)</span><span class="sxs-lookup"><span data-stu-id="de114-144">public void addMenuitem(WebMenuFunction webMenuFunction)</span></span>                 |                                                                                                                                               |

## <a name="method-changedby"></a><span data-ttu-id="de114-145">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="de114-145">Method changedBy</span></span>

<span data-ttu-id="de114-146">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-146">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="de114-147">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="de114-147">Parameters - changedBy</span></span>

<span data-ttu-id="de114-148">値</span><span class="sxs-lookup"><span data-stu-id="de114-148">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="de114-149">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="de114-149">Return Value - changedBy</span></span>

<span data-ttu-id="de114-150">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="de114-150">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="de114-151">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="de114-151">Method changedDate</span></span>

<span data-ttu-id="de114-152">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-152">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="de114-153">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="de114-153">Parameters - changedDate</span></span>

<span data-ttu-id="de114-154">値</span><span class="sxs-lookup"><span data-stu-id="de114-154">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="de114-155">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="de114-155">Return Value - changedDate</span></span>

<span data-ttu-id="de114-156">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="de114-156">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="de114-157">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="de114-157">Method changedTime</span></span>

<span data-ttu-id="de114-158">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-158">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="de114-159">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="de114-159">Parameters - changedTime</span></span>

<span data-ttu-id="de114-160">値</span><span class="sxs-lookup"><span data-stu-id="de114-160">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="de114-161">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="de114-161">Return Value - changedTime</span></span>

<span data-ttu-id="de114-162">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="de114-162">The time an application object was last changed.</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="de114-163">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="de114-163">Method configurationKey</span></span>

<span data-ttu-id="de114-164">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-164">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="de114-165">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="de114-165">Parameters - configurationKey</span></span>

<span data-ttu-id="de114-166">値</span><span class="sxs-lookup"><span data-stu-id="de114-166">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="de114-167">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="de114-167">Return Value - configurationKey</span></span>

<span data-ttu-id="de114-168">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="de114-168">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="de114-169">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="de114-169">Remarks - configurationKey</span></span>

<span data-ttu-id="de114-170">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de114-170">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="de114-171">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="de114-171">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="de114-172">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="de114-172">Method createdBy</span></span>

<span data-ttu-id="de114-173">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-173">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="de114-174">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="de114-174">Parameters - createdBy</span></span>

<span data-ttu-id="de114-175">値</span><span class="sxs-lookup"><span data-stu-id="de114-175">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="de114-176">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="de114-176">Return Value - createdBy</span></span>

<span data-ttu-id="de114-177">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="de114-177">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="de114-178">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="de114-178">Method creationDate</span></span>

<span data-ttu-id="de114-179">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-179">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="de114-180">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="de114-180">Parameters - creationDate</span></span>

<span data-ttu-id="de114-181">値</span><span class="sxs-lookup"><span data-stu-id="de114-181">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="de114-182">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="de114-182">Return Value - creationDate</span></span>

<span data-ttu-id="de114-183">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="de114-183">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="de114-184">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="de114-184">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="de114-185">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="de114-185">Parameters - creationTime</span></span>

<span data-ttu-id="de114-186">値</span><span class="sxs-lookup"><span data-stu-id="de114-186">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="de114-187">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="de114-187">Return Value - creationTime</span></span>

## <a name="method-highlightselected"></a><span data-ttu-id="de114-188">メソッド highlightSelected</span><span class="sxs-lookup"><span data-stu-id="de114-188">Method highlightSelected</span></span>

```xpp
public boolean highlightSelected([boolean value])
```

### <a name="parameters---highlightselected"></a><span data-ttu-id="de114-189">パラメーター - highlightSelected</span><span class="sxs-lookup"><span data-stu-id="de114-189">Parameters - highlightSelected</span></span>

<span data-ttu-id="de114-190">値</span><span class="sxs-lookup"><span data-stu-id="de114-190">value</span></span>  

### <a name="return-value---highlightselected"></a><span data-ttu-id="de114-191">戻り値 - highlightSelected</span><span class="sxs-lookup"><span data-stu-id="de114-191">Return Value - highlightSelected</span></span>

## <a name="method-label"></a><span data-ttu-id="de114-192">メソッド label</span><span class="sxs-lookup"><span data-stu-id="de114-192">Method label</span></span>

<span data-ttu-id="de114-193">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-193">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="de114-194">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="de114-194">Parameters - label</span></span>

<span data-ttu-id="de114-195">値</span><span class="sxs-lookup"><span data-stu-id="de114-195">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="de114-196">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="de114-196">Return Value - label</span></span>

<span data-ttu-id="de114-197">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="de114-197">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="de114-198">備考 - label</span><span class="sxs-lookup"><span data-stu-id="de114-198">Remarks - label</span></span>

<span data-ttu-id="de114-199">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="de114-199">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="de114-200">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="de114-200">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="de114-201">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="de114-201">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="de114-202">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="de114-202">Parameters - menuItemName</span></span>

<span data-ttu-id="de114-203">値</span><span class="sxs-lookup"><span data-stu-id="de114-203">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="de114-204">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="de114-204">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="de114-205">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="de114-205">Method menuItemType</span></span>

```xpp
public WebMenuItemType menuItemType([WebMenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="de114-206">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="de114-206">Parameters - menuItemType</span></span>

<span data-ttu-id="de114-207">値</span><span class="sxs-lookup"><span data-stu-id="de114-207">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="de114-208">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="de114-208">Return Value - menuItemType</span></span>

## <a name="method-menuname"></a><span data-ttu-id="de114-209">メソッド menuName</span><span class="sxs-lookup"><span data-stu-id="de114-209">Method menuName</span></span>

```xpp
public str menuName()
```

### <a name="return-value---menuname"></a><span data-ttu-id="de114-210">戻り値 - menuName</span><span class="sxs-lookup"><span data-stu-id="de114-210">Return Value - menuName</span></span>

## <a name="method-name"></a><span data-ttu-id="de114-211">メソッド名</span><span class="sxs-lookup"><span data-stu-id="de114-211">Method name</span></span>

<span data-ttu-id="de114-212">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-212">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="de114-213">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="de114-213">Parameters - name</span></span>

<span data-ttu-id="de114-214">値</span><span class="sxs-lookup"><span data-stu-id="de114-214">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="de114-215">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="de114-215">Return Value - name</span></span>

<span data-ttu-id="de114-216">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="de114-216">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="de114-217">備考 - name</span><span class="sxs-lookup"><span data-stu-id="de114-217">Remarks - name</span></span>

<span data-ttu-id="de114-218">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="de114-218">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="de114-219">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="de114-219">Begins with a letter.</span></span>
-   <span data-ttu-id="de114-220">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="de114-220">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="de114-221">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="de114-221">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="de114-222">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="de114-222">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="de114-223">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="de114-223">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, or classes.</span></span>

## <a name="method-neededaccesslevel"></a><span data-ttu-id="de114-224">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="de114-224">Method neededAccessLevel</span></span>

<span data-ttu-id="de114-225">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="de114-225">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

```xpp
public int neededAccessLevel([int value])
```

### <a name="parameters---neededaccesslevel"></a><span data-ttu-id="de114-226">パラメーター - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="de114-226">Parameters - neededAccessLevel</span></span>

<span data-ttu-id="de114-227">値</span><span class="sxs-lookup"><span data-stu-id="de114-227">value</span></span>  

### <a name="return-value---neededaccesslevel"></a><span data-ttu-id="de114-228">戻り値 - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="de114-228">Return Value - neededAccessLevel</span></span>

<span data-ttu-id="de114-229">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="de114-229">The current value of the neededAccessLevel property.</span></span>

### <a name="remarks---neededaccesslevel"></a><span data-ttu-id="de114-230">備考 - neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="de114-230">Remarks - neededAccessLevel</span></span>

<span data-ttu-id="de114-231">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="de114-231">The possible values for the AccessType system enumeration value are as follows:</span></span>

-   <span data-ttu-id="de114-232">AccessType::NoAccess</span><span class="sxs-lookup"><span data-stu-id="de114-232">AccessType::NoAccess</span></span>
-   <span data-ttu-id="de114-233">AccessType::View</span><span class="sxs-lookup"><span data-stu-id="de114-233">AccessType::View</span></span>
-   <span data-ttu-id="de114-234">AccessType::Edit</span><span class="sxs-lookup"><span data-stu-id="de114-234">AccessType::Edit</span></span>
-   <span data-ttu-id="de114-235">AccessType::Add</span><span class="sxs-lookup"><span data-stu-id="de114-235">AccessType::Add</span></span>
-   <span data-ttu-id="de114-236">AccessType::Delete</span><span class="sxs-lookup"><span data-stu-id="de114-236">AccessType::Delete</span></span>

## <a name="method-origin"></a><span data-ttu-id="de114-237">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="de114-237">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="de114-238">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="de114-238">Parameters - origin</span></span>

<span data-ttu-id="de114-239">値</span><span class="sxs-lookup"><span data-stu-id="de114-239">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="de114-240">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="de114-240">Return Value - origin</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="de114-241">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="de114-241">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="de114-242">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="de114-242">Parameters - securityKey</span></span>

<span data-ttu-id="de114-243">値</span><span class="sxs-lookup"><span data-stu-id="de114-243">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="de114-244">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="de114-244">Return Value - securityKey</span></span>

## <a name="method-setcompany"></a><span data-ttu-id="de114-245">メソッド setCompany</span><span class="sxs-lookup"><span data-stu-id="de114-245">Method setCompany</span></span>

```xpp
public boolean setCompany([boolean value])
```

### <a name="parameters---setcompany"></a><span data-ttu-id="de114-246">パラメーター - setCompany</span><span class="sxs-lookup"><span data-stu-id="de114-246">Parameters - setCompany</span></span>

<span data-ttu-id="de114-247">値</span><span class="sxs-lookup"><span data-stu-id="de114-247">value</span></span>  

### <a name="return-value---setcompany"></a><span data-ttu-id="de114-248">戻り値 - setCompany</span><span class="sxs-lookup"><span data-stu-id="de114-248">Return Value - setCompany</span></span>

## <a name="method-showparentmodule"></a><span data-ttu-id="de114-249">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="de114-249">Method showParentModule</span></span>

```xpp
public boolean showParentModule([boolean value])
```

### <a name="parameters---showparentmodule"></a><span data-ttu-id="de114-250">パラメーター - showParentModule</span><span class="sxs-lookup"><span data-stu-id="de114-250">Parameters - showParentModule</span></span>

<span data-ttu-id="de114-251">値</span><span class="sxs-lookup"><span data-stu-id="de114-251">value</span></span>  

### <a name="return-value---showparentmodule"></a><span data-ttu-id="de114-252">戻り値 - showParentModule</span><span class="sxs-lookup"><span data-stu-id="de114-252">Return Value - showParentModule</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="de114-253">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="de114-253">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="de114-254">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="de114-254">Parameters - webTarget</span></span>

<span data-ttu-id="de114-255">値</span><span class="sxs-lookup"><span data-stu-id="de114-255">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="de114-256">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="de114-256">Return Value - webTarget</span></span>

## <a name="method-addseparator"></a><span data-ttu-id="de114-257">メソッド addSeparator</span><span class="sxs-lookup"><span data-stu-id="de114-257">Method addSeparator</span></span>

```xpp
public void addSeparator()
```

## <a name="method-makemenu"></a><span data-ttu-id="de114-258">メソッド makeMenu</span><span class="sxs-lookup"><span data-stu-id="de114-258">Method makeMenu</span></span>

```xpp
public void makeMenu(Object outputClass)
```

### <a name="parameters---makemenu"></a><span data-ttu-id="de114-259">パラメーター - makeMenu</span><span class="sxs-lookup"><span data-stu-id="de114-259">Parameters - makeMenu</span></span>

<span data-ttu-id="de114-260">outputClass</span><span class="sxs-lookup"><span data-stu-id="de114-260">outputClass</span></span>  

## <a name="method-addsubmenu"></a><span data-ttu-id="de114-261">メソッド addSubmenu</span><span class="sxs-lookup"><span data-stu-id="de114-261">Method addSubmenu</span></span>

```xpp
public void addSubmenu(str name)
```

### <a name="parameters---addsubmenu"></a><span data-ttu-id="de114-262">パラメーター - addSubmenu</span><span class="sxs-lookup"><span data-stu-id="de114-262">Parameters - addSubmenu</span></span>

<span data-ttu-id="de114-263">名前</span><span class="sxs-lookup"><span data-stu-id="de114-263">name</span></span>  

## <a name="method-new"></a><span data-ttu-id="de114-264">メソッド new</span><span class="sxs-lookup"><span data-stu-id="de114-264">Method new</span></span>

<span data-ttu-id="de114-265">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="de114-265">Initializes a new instance of the TreeNode class.</span></span>

```xpp
public void new(str Name)
```

### <a name="parameters---new"></a><span data-ttu-id="de114-266">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="de114-266">Parameters - new</span></span>

<span data-ttu-id="de114-267">氏名</span><span class="sxs-lookup"><span data-stu-id="de114-267">Name</span></span>  

## <a name="method-addmenuitem"></a><span data-ttu-id="de114-268">メソッド addMenuitem</span><span class="sxs-lookup"><span data-stu-id="de114-268">Method addMenuitem</span></span>

```xpp
public void addMenuitem(WebMenuFunction webMenuFunction)
```

### <a name="parameters---addmenuitem"></a><span data-ttu-id="de114-269">パラメーター - addMenuitem</span><span class="sxs-lookup"><span data-stu-id="de114-269">Parameters - addMenuitem</span></span>

<span data-ttu-id="de114-270">webMenuFunction</span><span class="sxs-lookup"><span data-stu-id="de114-270">webMenuFunction</span></span>  

