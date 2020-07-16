---
title: DictFullTextIndex クラス
description: このトピックでは、DictFullTextIndex クラスについて説明します。
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
ms.openlocfilehash: eeea7ee61da8d6cc49f440dff77364f526f1aae9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502987"
---
# <a name="class-dictfulltextindex"></a><span data-ttu-id="8d3c1-103">クラス DictFullTextIndex</span><span class="sxs-lookup"><span data-stu-id="8d3c1-103">Class DictFullTextIndex</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictFullTextIndex extends Object
```

<span data-ttu-id="8d3c1-104">DictFullTextIndex クラスは、フル テキスト インデックスに関するメタデータを返します。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-104">The DictFullTextIndex class returns metadata about a full text index.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d3c1-105">備考</span><span class="sxs-lookup"><span data-stu-id="8d3c1-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="8d3c1-106">例</span><span class="sxs-lookup"><span data-stu-id="8d3c1-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="8d3c1-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="8d3c1-107">Methods</span></span>

| <span data-ttu-id="8d3c1-108">方法</span><span class="sxs-lookup"><span data-stu-id="8d3c1-108">Method</span></span>                                                  | <span data-ttu-id="8d3c1-109">説明</span><span class="sxs-lookup"><span data-stu-id="8d3c1-109">Description</span></span>                                            |
|---------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="8d3c1-110">public FullTextIndexChangeTracking changeTrackingMode()</span><span class="sxs-lookup"><span data-stu-id="8d3c1-110">public FullTextIndexChangeTracking changeTrackingMode()</span></span> | <span data-ttu-id="8d3c1-111">フル テキスト インデックスの変更追跡モードを取得します。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-111">Gets the change tracking mode of the full text index.</span></span>  |
| <span data-ttu-id="8d3c1-112">public ConfigurationKeyId configurationKeyId()</span><span class="sxs-lookup"><span data-stu-id="8d3c1-112">public ConfigurationKeyId configurationKeyId()</span></span>          | <span data-ttu-id="8d3c1-113">インデックスのコンフィギュレーション キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-113">Returns the ID of the configuration key for the index.</span></span> |
| <span data-ttu-id="8d3c1-114">public IndexId id()</span><span class="sxs-lookup"><span data-stu-id="8d3c1-114">public IndexId id()</span></span>                                     | <span data-ttu-id="8d3c1-115">フル テキスト インデックスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-115">Gets the ID of the full text index.</span></span>                    |
| <span data-ttu-id="8d3c1-116">public str name()</span><span class="sxs-lookup"><span data-stu-id="8d3c1-116">public str name()</span></span>                                       | <span data-ttu-id="8d3c1-117">フル テキスト インデックスの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-117">Gets the name of the full text index.</span></span>                  |
| <span data-ttu-id="8d3c1-118">public TableId tableid()</span><span class="sxs-lookup"><span data-stu-id="8d3c1-118">public TableId tableid()</span></span>                                | <span data-ttu-id="8d3c1-119">インデックスを含むテーブルの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-119">Returns the ID of the table that contains the index.</span></span>   |
| <span data-ttu-id="8d3c1-120">public void new(TableId tableId, IndexId indexId)</span><span class="sxs-lookup"><span data-stu-id="8d3c1-120">public void new(TableId tableId, IndexId indexId)</span></span>       | <span data-ttu-id="8d3c1-121">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-121">Initializes a new instance of the Object class.</span></span>        |

## <a name="method-changetrackingmode"></a><span data-ttu-id="8d3c1-122">メソッド changeTrackingMode</span><span class="sxs-lookup"><span data-stu-id="8d3c1-122">Method changeTrackingMode</span></span>

<span data-ttu-id="8d3c1-123">フル テキスト インデックスの変更追跡モードを取得します。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-123">Gets the change tracking mode of the full text index.</span></span>

```xpp
public FullTextIndexChangeTracking changeTrackingMode()
```

### <a name="return-value---changetrackingmode"></a><span data-ttu-id="8d3c1-124">戻り値 - changeTrackingMode</span><span class="sxs-lookup"><span data-stu-id="8d3c1-124">Return Value - changeTrackingMode</span></span>

## <a name="method-configurationkeyid"></a><span data-ttu-id="8d3c1-125">メソッド configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="8d3c1-125">Method configurationKeyId</span></span>

<span data-ttu-id="8d3c1-126">インデックスのコンフィギュレーション キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-126">Returns the ID of the configuration key for the index.</span></span>

```xpp
public ConfigurationKeyId configurationKeyId()
```

### <a name="return-value---configurationkeyid"></a><span data-ttu-id="8d3c1-127">戻り値 - configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="8d3c1-127">Return Value - configurationKeyId</span></span>

<span data-ttu-id="8d3c1-128">インデックスのコンフィギュレーション キーの ID。インデックスにコンフィギュレーション キーがない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-128">The ID of the configuration key for the index; 0 (zero) if the index does not have a configuration key.</span></span>

## <a name="method-id"></a><span data-ttu-id="8d3c1-129">メソッド id</span><span class="sxs-lookup"><span data-stu-id="8d3c1-129">Method id</span></span>

<span data-ttu-id="8d3c1-130">フル テキスト インデックスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-130">Gets the ID of the full text index.</span></span>

```xpp
public IndexId id()
```

### <a name="return-value---id"></a><span data-ttu-id="8d3c1-131">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="8d3c1-131">Return Value - id</span></span>

<span data-ttu-id="8d3c1-132">インデックスの ID です。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-132">The ID of the index.</span></span>

## <a name="method-name"></a><span data-ttu-id="8d3c1-133">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8d3c1-133">Method name</span></span>

<span data-ttu-id="8d3c1-134">フル テキスト インデックスの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-134">Gets the name of the full text index.</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="8d3c1-135">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="8d3c1-135">Return Value - name</span></span>

<span data-ttu-id="8d3c1-136">インデックスの名前。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-136">The name of the index.</span></span>

## <a name="method-tableid"></a><span data-ttu-id="8d3c1-137">メソッド tableid</span><span class="sxs-lookup"><span data-stu-id="8d3c1-137">Method tableid</span></span>

<span data-ttu-id="8d3c1-138">インデックスを含むテーブルの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-138">Returns the ID of the table that contains the index.</span></span>

```xpp
public TableId tableid()
```

### <a name="return-value---tableid"></a><span data-ttu-id="8d3c1-139">戻り値 - tableid</span><span class="sxs-lookup"><span data-stu-id="8d3c1-139">Return Value - tableid</span></span>

<span data-ttu-id="8d3c1-140">インデックスを含むテーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-140">The ID of the table that contains the index.</span></span>

## <a name="method-new"></a><span data-ttu-id="8d3c1-141">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8d3c1-141">Method new</span></span>

<span data-ttu-id="8d3c1-142">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8d3c1-142">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(TableId tableId, IndexId indexId)
```

### <a name="parameters---new"></a><span data-ttu-id="8d3c1-143">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="8d3c1-143">Parameters - new</span></span>

<span data-ttu-id="8d3c1-144">tableId</span><span class="sxs-lookup"><span data-stu-id="8d3c1-144">tableId</span></span>  

<!-- -->

<span data-ttu-id="8d3c1-145">indexId</span><span class="sxs-lookup"><span data-stu-id="8d3c1-145">indexId</span></span>  

