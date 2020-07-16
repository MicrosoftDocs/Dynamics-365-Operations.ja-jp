---
title: MenuItem クラス
description: このトピックでは､MenuItem クラスについて説明します。
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
ms.openlocfilehash: a4e6bf5ee11fa90aaa588becc193b1e34e35df04
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502577"
---
# <a name="class-menuitem"></a><span data-ttu-id="e8da9-103">クラス MenuItem</span><span class="sxs-lookup"><span data-stu-id="e8da9-103">Class MenuItem</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class MenuItem extends TreeNode
```

<span data-ttu-id="e8da9-104">MenuItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e8da9-104">The MenuItem class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8da9-105">備考</span><span class="sxs-lookup"><span data-stu-id="e8da9-105">Remarks</span></span>

<span data-ttu-id="e8da9-106">メニュー項目は、メニュー機能のユーザー インターフェイスを表します。</span><span class="sxs-lookup"><span data-stu-id="e8da9-106">A menu item represents the user interface of a menu function.</span></span> <span data-ttu-id="e8da9-107">メニュー項目は、ユーザーがメニュー項目を選択するときに実行される MenuFunction オブジェクトにリンクされます。</span><span class="sxs-lookup"><span data-stu-id="e8da9-107">Menu items are linked to a MenuFunction object, which runs when the user selects the menu item.</span></span> <span data-ttu-id="e8da9-108">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e8da9-108">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="e8da9-109">例</span><span class="sxs-lookup"><span data-stu-id="e8da9-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="e8da9-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="e8da9-110">Methods</span></span>

| <span data-ttu-id="e8da9-111">方法</span><span class="sxs-lookup"><span data-stu-id="e8da9-111">Method</span></span>                                                     | <span data-ttu-id="e8da9-112">説明</span><span class="sxs-lookup"><span data-stu-id="e8da9-112">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8da9-113">public str allowRootNavigation(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e8da9-113">public str allowRootNavigation(\[str value\])</span></span>              |                                                                                                                                               |
| <span data-ttu-id="e8da9-114">public boolean isDisplayedInContentArea(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="e8da9-114">public boolean isDisplayedInContentArea(\[boolean value\])</span></span> |                                                                                                                                               |
| <span data-ttu-id="e8da9-115">public str label(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="e8da9-115">public str label(\[str name\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="e8da9-116">public str menuFunctionName(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="e8da9-116">public str menuFunctionName(\[str name\])</span></span>                  |                                                                                                                                               |
| <span data-ttu-id="e8da9-117">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e8da9-117">public str menuItemName(\[str value\])</span></span>                     |                                                                                                                                               |
| <span data-ttu-id="e8da9-118">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="e8da9-118">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>   |                                                                                                                                               |
| <span data-ttu-id="e8da9-119">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e8da9-119">public str name(\[str value\])</span></span>                             | <span data-ttu-id="e8da9-120">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8da9-120">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="e8da9-121">public str parameter(\[str parameter\])</span><span class="sxs-lookup"><span data-stu-id="e8da9-121">public str parameter(\[str parameter\])</span></span>                    |                                                                                                                                               |
| <span data-ttu-id="e8da9-122">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e8da9-122">public str parameters(\[str value\])</span></span>                       | <span data-ttu-id="e8da9-123">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8da9-123">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                        |
| <span data-ttu-id="e8da9-124">public str shortCut(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e8da9-124">public str shortCut(\[str value\])</span></span>                         |                                                                                                                                               |
| <span data-ttu-id="e8da9-125">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="e8da9-125">public boolean showParentModule(\[boolean value\])</span></span>         |                                                                                                                                               |
| <span data-ttu-id="e8da9-126">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="e8da9-126">public boolean visible(\[boolean value\])</span></span>                  |                                                                                                                                               |
| <span data-ttu-id="e8da9-127">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="e8da9-127">public str webTarget(\[str value\])</span></span>                        |                                                                                                                                               |

## <a name="method-allowrootnavigation"></a><span data-ttu-id="e8da9-128">メソッド allowRootNavigation</span><span class="sxs-lookup"><span data-stu-id="e8da9-128">Method allowRootNavigation</span></span>

```xpp
public str allowRootNavigation([str value])
```

### <a name="parameters---allowrootnavigation"></a><span data-ttu-id="e8da9-129">パラメーター - allowRootNavigation</span><span class="sxs-lookup"><span data-stu-id="e8da9-129">Parameters - allowRootNavigation</span></span>

<span data-ttu-id="e8da9-130">値</span><span class="sxs-lookup"><span data-stu-id="e8da9-130">value</span></span>  

### <a name="return-value---allowrootnavigation"></a><span data-ttu-id="e8da9-131">戻り値 - allowRootNavigation</span><span class="sxs-lookup"><span data-stu-id="e8da9-131">Return Value - allowRootNavigation</span></span>

## <a name="method-isdisplayedincontentarea"></a><span data-ttu-id="e8da9-132">メソッド isDisplayedInContentArea</span><span class="sxs-lookup"><span data-stu-id="e8da9-132">Method isDisplayedInContentArea</span></span>

```xpp
public boolean isDisplayedInContentArea([boolean value])
```

### <a name="parameters---isdisplayedincontentarea"></a><span data-ttu-id="e8da9-133">パラメーター - isDisplayedInContentArea</span><span class="sxs-lookup"><span data-stu-id="e8da9-133">Parameters - isDisplayedInContentArea</span></span>

<span data-ttu-id="e8da9-134">値</span><span class="sxs-lookup"><span data-stu-id="e8da9-134">value</span></span>  

### <a name="return-value---isdisplayedincontentarea"></a><span data-ttu-id="e8da9-135">戻り値 - isDisplayedInContentArea</span><span class="sxs-lookup"><span data-stu-id="e8da9-135">Return Value - isDisplayedInContentArea</span></span>

## <a name="method-label"></a><span data-ttu-id="e8da9-136">メソッド label</span><span class="sxs-lookup"><span data-stu-id="e8da9-136">Method label</span></span>

```xpp
public str label([str name])
```

### <a name="parameters---label"></a><span data-ttu-id="e8da9-137">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="e8da9-137">Parameters - label</span></span>

<span data-ttu-id="e8da9-138">名前</span><span class="sxs-lookup"><span data-stu-id="e8da9-138">name</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="e8da9-139">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="e8da9-139">Return Value - label</span></span>

## <a name="method-menufunctionname"></a><span data-ttu-id="e8da9-140">メソッド menuFunctionName</span><span class="sxs-lookup"><span data-stu-id="e8da9-140">Method menuFunctionName</span></span>

```xpp
public str menuFunctionName([str name])
```

### <a name="parameters---menufunctionname"></a><span data-ttu-id="e8da9-141">パラメーター - menuFunctionName</span><span class="sxs-lookup"><span data-stu-id="e8da9-141">Parameters - menuFunctionName</span></span>

<span data-ttu-id="e8da9-142">名前</span><span class="sxs-lookup"><span data-stu-id="e8da9-142">name</span></span>  

### <a name="return-value---menufunctionname"></a><span data-ttu-id="e8da9-143">戻り値 - menuFunctionName</span><span class="sxs-lookup"><span data-stu-id="e8da9-143">Return Value - menuFunctionName</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="e8da9-144">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="e8da9-144">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="e8da9-145">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="e8da9-145">Parameters - menuItemName</span></span>

<span data-ttu-id="e8da9-146">値</span><span class="sxs-lookup"><span data-stu-id="e8da9-146">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="e8da9-147">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="e8da9-147">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="e8da9-148">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="e8da9-148">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="e8da9-149">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="e8da9-149">Parameters - menuItemType</span></span>

<span data-ttu-id="e8da9-150">値</span><span class="sxs-lookup"><span data-stu-id="e8da9-150">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="e8da9-151">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="e8da9-151">Return Value - menuItemType</span></span>

## <a name="method-name"></a><span data-ttu-id="e8da9-152">メソッド名</span><span class="sxs-lookup"><span data-stu-id="e8da9-152">Method name</span></span>

<span data-ttu-id="e8da9-153">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8da9-153">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="e8da9-154">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="e8da9-154">Parameters - name</span></span>

<span data-ttu-id="e8da9-155">値</span><span class="sxs-lookup"><span data-stu-id="e8da9-155">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="e8da9-156">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="e8da9-156">Return Value - name</span></span>

<span data-ttu-id="e8da9-157">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="e8da9-157">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="e8da9-158">備考 - name</span><span class="sxs-lookup"><span data-stu-id="e8da9-158">Remarks - name</span></span>

<span data-ttu-id="e8da9-159">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8da9-159">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="e8da9-160">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="e8da9-160">Begins with a letter.</span></span>
-   <span data-ttu-id="e8da9-161">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="e8da9-161">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="e8da9-162">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="e8da9-162">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="e8da9-163">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="e8da9-163">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="e8da9-164">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="e8da9-164">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-parameter"></a><span data-ttu-id="e8da9-165">メソッド parameter</span><span class="sxs-lookup"><span data-stu-id="e8da9-165">Method parameter</span></span>

```xpp
public str parameter([str parameter])
```

### <a name="parameters---parameter"></a><span data-ttu-id="e8da9-166">パラメーター - parameter</span><span class="sxs-lookup"><span data-stu-id="e8da9-166">Parameters - parameter</span></span>

<span data-ttu-id="e8da9-167">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e8da9-167">parameter</span></span>  

### <a name="return-value---parameter"></a><span data-ttu-id="e8da9-168">戻り値 - パラメータ</span><span class="sxs-lookup"><span data-stu-id="e8da9-168">Return Value - parameter</span></span>

## <a name="method-parameters"></a><span data-ttu-id="e8da9-169">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="e8da9-169">Method parameters</span></span>

<span data-ttu-id="e8da9-170">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e8da9-170">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="e8da9-171">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="e8da9-171">Parameters - parameters</span></span>

<span data-ttu-id="e8da9-172">値</span><span class="sxs-lookup"><span data-stu-id="e8da9-172">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="e8da9-173">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="e8da9-173">Return Value - parameters</span></span>

<span data-ttu-id="e8da9-174">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="e8da9-174">The list of parameters that are passed to the object.</span></span>

### <a name="remarks---parameters"></a><span data-ttu-id="e8da9-175">備考 - パラメータ</span><span class="sxs-lookup"><span data-stu-id="e8da9-175">Remarks - parameters</span></span>

<span data-ttu-id="e8da9-176">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="e8da9-176">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="e8da9-177">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="e8da9-177">Objects ignore passed, unrecognized parameters.</span></span>

## <a name="method-shortcut"></a><span data-ttu-id="e8da9-178">メソッド shortCut</span><span class="sxs-lookup"><span data-stu-id="e8da9-178">Method shortCut</span></span>

```xpp
public str shortCut([str value])
```

### <a name="parameters---shortcut"></a><span data-ttu-id="e8da9-179">パラメーター - shortCut </span><span class="sxs-lookup"><span data-stu-id="e8da9-179">Parameters - shortCut</span></span>

<span data-ttu-id="e8da9-180">値</span><span class="sxs-lookup"><span data-stu-id="e8da9-180">value</span></span>  

### <a name="return-value---shortcut"></a><span data-ttu-id="e8da9-181">戻り値 - shortCut</span><span class="sxs-lookup"><span data-stu-id="e8da9-181">Return Value - shortCut</span></span>

## <a name="method-showparentmodule"></a><span data-ttu-id="e8da9-182">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="e8da9-182">Method showParentModule</span></span>

```xpp
public boolean showParentModule([boolean value])
```

### <a name="parameters---showparentmodule"></a><span data-ttu-id="e8da9-183">パラメーター - showParentModule</span><span class="sxs-lookup"><span data-stu-id="e8da9-183">Parameters - showParentModule</span></span>

<span data-ttu-id="e8da9-184">値</span><span class="sxs-lookup"><span data-stu-id="e8da9-184">value</span></span>  

### <a name="return-value---showparentmodule"></a><span data-ttu-id="e8da9-185">戻り値 - showParentModule</span><span class="sxs-lookup"><span data-stu-id="e8da9-185">Return Value - showParentModule</span></span>

## <a name="method-visible"></a><span data-ttu-id="e8da9-186">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="e8da9-186">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="e8da9-187">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="e8da9-187">Parameters - visible</span></span>

<span data-ttu-id="e8da9-188">値</span><span class="sxs-lookup"><span data-stu-id="e8da9-188">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="e8da9-189">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="e8da9-189">Return Value - visible</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="e8da9-190">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="e8da9-190">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="e8da9-191">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="e8da9-191">Parameters - webTarget</span></span>

<span data-ttu-id="e8da9-192">値</span><span class="sxs-lookup"><span data-stu-id="e8da9-192">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="e8da9-193">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="e8da9-193">Return Value - webTarget</span></span>

