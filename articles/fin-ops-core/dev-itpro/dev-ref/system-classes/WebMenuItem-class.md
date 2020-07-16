---
title: WebMenuItem クラス
description: このトピックでは、WebMenuItem クラスについて説明します。
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
ms.openlocfilehash: cde752849e0e198156be7bbfc5c48af26e5abc15
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503001"
---
# <a name="class-webmenuitem"></a><span data-ttu-id="8c0c8-103">クラス WebMenuItem</span><span class="sxs-lookup"><span data-stu-id="8c0c8-103">Class WebMenuItem</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class WebMenuItem extends TreeNode
```

<span data-ttu-id="8c0c8-104">WebMenuItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-104">The WebMenuItem class enables you to create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c0c8-105">備考</span><span class="sxs-lookup"><span data-stu-id="8c0c8-105">Remarks</span></span>

<span data-ttu-id="8c0c8-106">このクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-106">This class enables you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="8c0c8-107">この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-107">Make sure that the user has access to the development security key (SysDevelopment) before you call this API.</span></span>

## <a name="examples"></a><span data-ttu-id="8c0c8-108">例</span><span class="sxs-lookup"><span data-stu-id="8c0c8-108">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="8c0c8-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="8c0c8-109">Methods</span></span>

| <span data-ttu-id="8c0c8-110">方法</span><span class="sxs-lookup"><span data-stu-id="8c0c8-110">Method</span></span>                                                         | <span data-ttu-id="8c0c8-111">説明</span><span class="sxs-lookup"><span data-stu-id="8c0c8-111">Description</span></span>                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0c8-112">public str label()</span><span class="sxs-lookup"><span data-stu-id="8c0c8-112">public str label()</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="8c0c8-113">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8c0c8-113">public str menuItemName(\[str value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="8c0c8-114">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="8c0c8-114">public WebMenuItemType menuItemType(\[WebMenuItemType value\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="8c0c8-115">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8c0c8-115">public str name(\[str value\])</span></span>                                 | <span data-ttu-id="8c0c8-116">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-116">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="8c0c8-117">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8c0c8-117">public str parameters(\[str value\])</span></span>                           | <span data-ttu-id="8c0c8-118">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-118">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                    |
| <span data-ttu-id="8c0c8-119">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="8c0c8-119">public boolean showParentModule(\[boolean value\])</span></span>             |                                                                                                                                           |

## <a name="method-label"></a><span data-ttu-id="8c0c8-120">メソッド label</span><span class="sxs-lookup"><span data-stu-id="8c0c8-120">Method label</span></span>

```xpp
public str label()
```

### <a name="return-value---label"></a><span data-ttu-id="8c0c8-121">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="8c0c8-121">Return Value - label</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="8c0c8-122">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="8c0c8-122">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="8c0c8-123">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="8c0c8-123">Parameters - menuItemName</span></span>

<span data-ttu-id="8c0c8-124">値</span><span class="sxs-lookup"><span data-stu-id="8c0c8-124">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="8c0c8-125">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="8c0c8-125">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="8c0c8-126">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="8c0c8-126">Method menuItemType</span></span>

```xpp
public WebMenuItemType menuItemType([WebMenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="8c0c8-127">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="8c0c8-127">Parameters - menuItemType</span></span>

<span data-ttu-id="8c0c8-128">値</span><span class="sxs-lookup"><span data-stu-id="8c0c8-128">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="8c0c8-129">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="8c0c8-129">Return Value - menuItemType</span></span>

## <a name="method-name"></a><span data-ttu-id="8c0c8-130">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8c0c8-130">Method name</span></span>

<span data-ttu-id="8c0c8-131">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-131">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="8c0c8-132">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="8c0c8-132">Parameters - name</span></span>

<span data-ttu-id="8c0c8-133">値</span><span class="sxs-lookup"><span data-stu-id="8c0c8-133">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="8c0c8-134">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="8c0c8-134">Return Value - name</span></span>

<span data-ttu-id="8c0c8-135">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-135">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="8c0c8-136">備考 - name</span><span class="sxs-lookup"><span data-stu-id="8c0c8-136">Remarks - name</span></span>

<span data-ttu-id="8c0c8-137">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-137">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="8c0c8-138">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-138">Begins with a letter.</span></span>
-   <span data-ttu-id="8c0c8-139">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-139">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="8c0c8-140">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-140">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="8c0c8-141">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-141">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="8c0c8-142">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-142">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-parameters"></a><span data-ttu-id="8c0c8-143">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="8c0c8-143">Method parameters</span></span>

<span data-ttu-id="8c0c8-144">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-144">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="8c0c8-145">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="8c0c8-145">Parameters - parameters</span></span>

<span data-ttu-id="8c0c8-146">値</span><span class="sxs-lookup"><span data-stu-id="8c0c8-146">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="8c0c8-147">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="8c0c8-147">Return Value - parameters</span></span>

<span data-ttu-id="8c0c8-148">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-148">The list of parameters that are passed to the object.</span></span>

### <a name="remarks---parameters"></a><span data-ttu-id="8c0c8-149">備考 - parameters</span><span class="sxs-lookup"><span data-stu-id="8c0c8-149">Remarks - parameters</span></span>

<span data-ttu-id="8c0c8-150">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-150">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="8c0c8-151">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-151">Objects ignore passed, unrecognized parameters.</span></span>

## <a name="method-showparentmodule"></a><span data-ttu-id="8c0c8-152">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="8c0c8-152">Method showParentModule</span></span>

```xpp
public boolean showParentModule([boolean value])
```

### <a name="parameters---showparentmodule"></a><span data-ttu-id="8c0c8-153">パラメーター - showParentModule</span><span class="sxs-lookup"><span data-stu-id="8c0c8-153">Parameters - showParentModule</span></span>

<span data-ttu-id="8c0c8-154">値</span><span class="sxs-lookup"><span data-stu-id="8c0c8-154">value</span></span>  

### <a name="return-value---showparentmodule"></a><span data-ttu-id="8c0c8-155">戻り値 - showParentModule</span><span class="sxs-lookup"><span data-stu-id="8c0c8-155">Return Value - showParentModule</span></span>

