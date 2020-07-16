---
title: UtilFile クラス
description: このトピックでは、UtilFile クラスについて説明します。
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
ms.openlocfilehash: 09a89fec9372dc62abbf9a9441624d70293e6951
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502780"
---
# <a name="class-utilfile"></a><span data-ttu-id="a385b-103">クラス UtilFile</span><span class="sxs-lookup"><span data-stu-id="a385b-103">Class UtilFile</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class UtilFile extends Object
```

## <a name="remarks"></a><span data-ttu-id="a385b-104">備考</span><span class="sxs-lookup"><span data-stu-id="a385b-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="a385b-105">例</span><span class="sxs-lookup"><span data-stu-id="a385b-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="a385b-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="a385b-106">Methods</span></span>

| <span data-ttu-id="a385b-107">方法</span><span class="sxs-lookup"><span data-stu-id="a385b-107">Method</span></span>                                                      | <span data-ttu-id="a385b-108">説明</span><span class="sxs-lookup"><span data-stu-id="a385b-108">Description</span></span>                                                      |
|-------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="a385b-109">public boolean aodFileExist(UtilEntryLevel layer)</span><span class="sxs-lookup"><span data-stu-id="a385b-109">public boolean aodFileExist(UtilEntryLevel layer)</span></span>           |                                                                  |
| <span data-ttu-id="a385b-110">public int importAODFile(UtilEntryLevel layer, int modelId)</span><span class="sxs-lookup"><span data-stu-id="a385b-110">public int importAODFile(UtilEntryLevel layer, int modelId)</span></span> |                                                                  |
| <span data-ttu-id="a385b-111">public str layers()</span><span class="sxs-lookup"><span data-stu-id="a385b-111">public str layers()</span></span>                                         |                                                                  |
| <span data-ttu-id="a385b-112">public boolean needReindex()</span><span class="sxs-lookup"><span data-stu-id="a385b-112">public boolean needReindex()</span></span>                                |                                                                  |
| <span data-ttu-id="a385b-113">public void check(str layer, str action)</span><span class="sxs-lookup"><span data-stu-id="a385b-113">public void check(str layer, str action)</span></span>                    |                                                                  |
| <span data-ttu-id="a385b-114">public void new(str fileType)</span><span class="sxs-lookup"><span data-stu-id="a385b-114">public void new(str fileType)</span></span>                               | <span data-ttu-id="a385b-115">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a385b-115">Initializes a new instance of the Object class.</span></span>                  |
| <span data-ttu-id="a385b-116">public void reindex()</span><span class="sxs-lookup"><span data-stu-id="a385b-116">public void reindex()</span></span>                                       | <span data-ttu-id="a385b-117">X++ コードとメタデータの作成、読み取り、更新、および削除ができます。</span><span class="sxs-lookup"><span data-stu-id="a385b-117">Lets you create, read, update, and delete X++ code and metadata.</span></span> |
| <span data-ttu-id="a385b-118">public void flushCache()</span><span class="sxs-lookup"><span data-stu-id="a385b-118">public void flushCache()</span></span>                                    |                                                                  |

## <a name="method-aodfileexist"></a><span data-ttu-id="a385b-119">メソッド aodFileExist</span><span class="sxs-lookup"><span data-stu-id="a385b-119">Method aodFileExist</span></span>

```xpp
public boolean aodFileExist(UtilEntryLevel layer)
```

### <a name="parameters---aodfileexist"></a><span data-ttu-id="a385b-120">パラメーター - aodFileExist</span><span class="sxs-lookup"><span data-stu-id="a385b-120">Parameters - aodFileExist</span></span>

<span data-ttu-id="a385b-121"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="a385b-121">layer</span></span>  

### <a name="return-value---aodfileexist"></a><span data-ttu-id="a385b-122">戻り値 - aodFileExist</span><span class="sxs-lookup"><span data-stu-id="a385b-122">Return Value - aodFileExist</span></span>

## <a name="method-importaodfile"></a><span data-ttu-id="a385b-123">メソッド importAODFile</span><span class="sxs-lookup"><span data-stu-id="a385b-123">Method importAODFile</span></span>

```xpp
public int importAODFile(UtilEntryLevel layer, int modelId)
```

### <a name="parameters---importaodfile"></a><span data-ttu-id="a385b-124">パラメーター - importAODFile</span><span class="sxs-lookup"><span data-stu-id="a385b-124">Parameters - importAODFile</span></span>

<span data-ttu-id="a385b-125"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="a385b-125">layer</span></span>  

<!-- -->

<span data-ttu-id="a385b-126">modelId</span><span class="sxs-lookup"><span data-stu-id="a385b-126">modelId</span></span>  

### <a name="return-value---importaodfile"></a><span data-ttu-id="a385b-127">戻り値 - importAODFile</span><span class="sxs-lookup"><span data-stu-id="a385b-127">Return Value - importAODFile</span></span>

## <a name="method-layers"></a><span data-ttu-id="a385b-128">メソッド layers</span><span class="sxs-lookup"><span data-stu-id="a385b-128">Method layers</span></span>

```xpp
public str layers()
```

### <a name="return-value---layers"></a><span data-ttu-id="a385b-129">戻り値 - layers</span><span class="sxs-lookup"><span data-stu-id="a385b-129">Return Value - layers</span></span>

## <a name="method-needreindex"></a><span data-ttu-id="a385b-130">メソッド needReindex</span><span class="sxs-lookup"><span data-stu-id="a385b-130">Method needReindex</span></span>

```xpp
public boolean needReindex()
```

### <a name="return-value---needreindex"></a><span data-ttu-id="a385b-131">戻り値 - needReindex</span><span class="sxs-lookup"><span data-stu-id="a385b-131">Return Value - needReindex</span></span>

## <a name="method-check"></a><span data-ttu-id="a385b-132">メソッド check</span><span class="sxs-lookup"><span data-stu-id="a385b-132">Method check</span></span>

```xpp
public void check(str layer, str action)
```

### <a name="parameters---check"></a><span data-ttu-id="a385b-133">パラメーター - check</span><span class="sxs-lookup"><span data-stu-id="a385b-133">Parameters - check</span></span>

<span data-ttu-id="a385b-134"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="a385b-134">layer</span></span>  

<!-- -->

<span data-ttu-id="a385b-135">アクション</span><span class="sxs-lookup"><span data-stu-id="a385b-135">action</span></span>  

## <a name="method-new"></a><span data-ttu-id="a385b-136">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a385b-136">Method new</span></span>

<span data-ttu-id="a385b-137">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a385b-137">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(str fileType)
```

### <a name="parameters---new"></a><span data-ttu-id="a385b-138">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="a385b-138">Parameters - new</span></span>

<span data-ttu-id="a385b-139">fileType</span><span class="sxs-lookup"><span data-stu-id="a385b-139">fileType</span></span>  

## <a name="method-reindex"></a><span data-ttu-id="a385b-140">メソッド reindex</span><span class="sxs-lookup"><span data-stu-id="a385b-140">Method reindex</span></span>

<span data-ttu-id="a385b-141">X++ コードとメタデータの作成、読み取り、更新、および削除ができます。</span><span class="sxs-lookup"><span data-stu-id="a385b-141">Lets you create, read, update, and delete X++ code and metadata.</span></span>

```xpp
public void reindex()
```

### <a name="remarks---reindex"></a><span data-ttu-id="a385b-142">備考 - reindex</span><span class="sxs-lookup"><span data-stu-id="a385b-142">Remarks - reindex</span></span>

<span data-ttu-id="a385b-143">この API を呼び出す前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a385b-143">Make sure that the user has access to the development security key (SysDevelopment) before you call this API.</span></span>

### <a name="examples---reindex"></a><span data-ttu-id="a385b-144">例 - reindex</span><span class="sxs-lookup"><span data-stu-id="a385b-144">Examples - reindex</span></span>

<span data-ttu-id="a385b-145">次の例では、UtilFile.reindex メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a385b-145">The following example calls the UtilFile.reindex method.</span></span> <span data-ttu-id="a385b-146">変更を実行する前に、ユーザーが必要なセキュリティ キーを持っているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a385b-146">It checks whether the user has the required security key before you perform a modification.</span></span>

```xpp
server static public void Main(Args _args) 
{ 
    UtilFile u; 
    u = new UtilFile("util"); 
    if (u) 
    { 
        u.reindex(); 
    } 
}
```

## <a name="method-flushcache"></a><span data-ttu-id="a385b-147">メソッド flushCache</span><span class="sxs-lookup"><span data-stu-id="a385b-147">Method flushCache</span></span>

```xpp
public void flushCache()
```


