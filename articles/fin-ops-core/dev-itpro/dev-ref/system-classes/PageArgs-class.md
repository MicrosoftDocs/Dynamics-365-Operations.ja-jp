---
title: PageArgs クラス
description: このトピックでは、PageArgs クラスについて説明します。
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
ms.openlocfilehash: 9b7ddb948842b519de3ca79c9eeaec73db5a59fb
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502539"
---
# <a name="class-pageargs"></a><span data-ttu-id="6f498-103">クラス PageArgs</span><span class="sxs-lookup"><span data-stu-id="6f498-103">Class PageArgs</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class PageArgs extends Object
```

<span data-ttu-id="6f498-104">PageArgs クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="6f498-104">The PageArgs class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f498-105">備考</span><span class="sxs-lookup"><span data-stu-id="6f498-105">Remarks</span></span>

<span data-ttu-id="6f498-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6f498-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="6f498-107">例</span><span class="sxs-lookup"><span data-stu-id="6f498-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="6f498-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="6f498-108">Methods</span></span>

| <span data-ttu-id="6f498-109">方法</span><span class="sxs-lookup"><span data-stu-id="6f498-109">Method</span></span>                                         | <span data-ttu-id="6f498-110">説明</span><span class="sxs-lookup"><span data-stu-id="6f498-110">Description</span></span>                                                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f498-111">public int enumParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6f498-111">public int enumParameter(\[int value\])</span></span>        | <span data-ttu-id="6f498-112">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6f498-112">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span> |
| <span data-ttu-id="6f498-113">public int enumTypeParameter(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6f498-113">public int enumTypeParameter(\[int value\])</span></span>    | <span data-ttu-id="6f498-114">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6f498-114">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>                                     |
| <span data-ttu-id="6f498-115">public Common externalRecord(\[Common value\])</span><span class="sxs-lookup"><span data-stu-id="6f498-115">public Common externalRecord(\[Common value\])</span></span> |                                                                                                             |
| <span data-ttu-id="6f498-116">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6f498-116">public str menuItemName(\[str value\])</span></span>         |                                                                                                             |
| <span data-ttu-id="6f498-117">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6f498-117">public str parameters(\[str value\])</span></span>           | <span data-ttu-id="6f498-118">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6f498-118">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>      |
| <span data-ttu-id="6f498-119">public void new()</span><span class="sxs-lookup"><span data-stu-id="6f498-119">public void new()</span></span>                              | <span data-ttu-id="6f498-120">PageArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6f498-120">Initializes a new instance of the PageArgs class.</span></span>                                                           |

## <a name="method-enumparameter"></a><span data-ttu-id="6f498-121">メソッド enumParameter</span><span class="sxs-lookup"><span data-stu-id="6f498-121">Method enumParameter</span></span>

<span data-ttu-id="6f498-122">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6f498-122">Gets or sets the enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

```xpp
public int enumParameter([int value])
```

### <a name="parameters---enumparameter"></a><span data-ttu-id="6f498-123">パラメーター - enumParameter</span><span class="sxs-lookup"><span data-stu-id="6f498-123">Parameters - enumParameter</span></span>

<span data-ttu-id="6f498-124">値</span><span class="sxs-lookup"><span data-stu-id="6f498-124">value</span></span>  

### <a name="return-value---enumparameter"></a><span data-ttu-id="6f498-125">戻り値 - enumParameter</span><span class="sxs-lookup"><span data-stu-id="6f498-125">Return Value - enumParameter</span></span>

<span data-ttu-id="6f498-126">MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="6f498-126">The enumParameter property that is passed to the object that is run by the MenuFunction class.</span></span>

## <a name="method-enumtypeparameter"></a><span data-ttu-id="6f498-127">メソッド enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="6f498-127">Method enumTypeParameter</span></span>

<span data-ttu-id="6f498-128">MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6f498-128">Gets or sets the enumTypeParameter property for the MenuFunction class.</span></span>

```xpp
public int enumTypeParameter([int value])
```

### <a name="parameters---enumtypeparameter"></a><span data-ttu-id="6f498-129">パラメーター - enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="6f498-129">Parameters - enumTypeParameter</span></span>

<span data-ttu-id="6f498-130">値</span><span class="sxs-lookup"><span data-stu-id="6f498-130">value</span></span>  

### <a name="return-value---enumtypeparameter"></a><span data-ttu-id="6f498-131">戻り値 - enumTypeParameter</span><span class="sxs-lookup"><span data-stu-id="6f498-131">Return Value - enumTypeParameter</span></span>

<span data-ttu-id="6f498-132">MenuFunction クラスの enumTypeParameter プロパティ。</span><span class="sxs-lookup"><span data-stu-id="6f498-132">The enumTypeParameter property for the MenuFunction class.</span></span>

## <a name="method-externalrecord"></a><span data-ttu-id="6f498-133">メソッド externalRecord</span><span class="sxs-lookup"><span data-stu-id="6f498-133">Method externalRecord</span></span>

```xpp
public Common externalRecord([Common value])
```

### <a name="parameters---externalrecord"></a><span data-ttu-id="6f498-134">パラメーター - externalRecord</span><span class="sxs-lookup"><span data-stu-id="6f498-134">Parameters - externalRecord</span></span>

<span data-ttu-id="6f498-135">値</span><span class="sxs-lookup"><span data-stu-id="6f498-135">value</span></span>  

### <a name="return-value---externalrecord"></a><span data-ttu-id="6f498-136">戻り値 - externalRecord</span><span class="sxs-lookup"><span data-stu-id="6f498-136">Return Value - externalRecord</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="6f498-137">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="6f498-137">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="6f498-138">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="6f498-138">Parameters - menuItemName</span></span>

<span data-ttu-id="6f498-139">値</span><span class="sxs-lookup"><span data-stu-id="6f498-139">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="6f498-140">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="6f498-140">Return Value - menuItemName</span></span>

## <a name="method-parameters"></a><span data-ttu-id="6f498-141">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="6f498-141">Method parameters</span></span>

<span data-ttu-id="6f498-142">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6f498-142">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a><span data-ttu-id="6f498-143">パラメーター - parameters</span><span class="sxs-lookup"><span data-stu-id="6f498-143">Parameters - parameters</span></span>

<span data-ttu-id="6f498-144">値</span><span class="sxs-lookup"><span data-stu-id="6f498-144">value</span></span>  

### <a name="return-value---parameters"></a><span data-ttu-id="6f498-145">戻り値 - parameters</span><span class="sxs-lookup"><span data-stu-id="6f498-145">Return Value - parameters</span></span>

<span data-ttu-id="6f498-146">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="6f498-146">The list of parameters that are passed to the object.</span></span>

### <a name="remarks---parameters"></a><span data-ttu-id="6f498-147">備考 - パラメータ</span><span class="sxs-lookup"><span data-stu-id="6f498-147">Remarks - parameters</span></span>

<span data-ttu-id="6f498-148">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="6f498-148">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="6f498-149">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="6f498-149">Objects ignore passed, unrecognized parameters.</span></span>

## <a name="method-new"></a><span data-ttu-id="6f498-150">メソッド new</span><span class="sxs-lookup"><span data-stu-id="6f498-150">Method new</span></span>

<span data-ttu-id="6f498-151">PageArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6f498-151">Initializes a new instance of the PageArgs class.</span></span>

```xpp
public void new()
```

