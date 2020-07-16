---
title: DictTableMap クラス
description: このトピックでは、DictTableMap クラスについて説明します。
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
ms.openlocfilehash: cbdfc6a2624d6129f29862f45e5964517162bbe5
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502675"
---
# <a name="class-dicttablemap"></a><span data-ttu-id="b03cf-103">クラス DictTableMap</span><span class="sxs-lookup"><span data-stu-id="b03cf-103">Class DictTableMap</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictTableMap extends Object
```

<span data-ttu-id="b03cf-104">DictTableMap クラスは、テーブル マッピングに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="b03cf-104">The DictTableMap class provides information about a table mapping.</span></span>

## <a name="remarks"></a><span data-ttu-id="b03cf-105">備考</span><span class="sxs-lookup"><span data-stu-id="b03cf-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="b03cf-106">例</span><span class="sxs-lookup"><span data-stu-id="b03cf-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b03cf-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="b03cf-107">Methods</span></span>

| <span data-ttu-id="b03cf-108">方法</span><span class="sxs-lookup"><span data-stu-id="b03cf-108">Method</span></span>                                 | <span data-ttu-id="b03cf-109">説明</span><span class="sxs-lookup"><span data-stu-id="b03cf-109">Description</span></span>                                                    |
|----------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b03cf-110">public int table()</span><span class="sxs-lookup"><span data-stu-id="b03cf-110">public int table()</span></span>                     | <span data-ttu-id="b03cf-111">マッピングが参照するテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="b03cf-111">Retrieves the table that the mapping references.</span></span>               |
| <span data-ttu-id="b03cf-112">public int fieldCnt()</span><span class="sxs-lookup"><span data-stu-id="b03cf-112">public int fieldCnt()</span></span>                  | <span data-ttu-id="b03cf-113">テーブル マッピングのフィールドの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="b03cf-113">Retrieves the count of fields in the table mapping.</span></span>            |
| <span data-ttu-id="b03cf-114">public int fieldCnt2FieldTo(int cnt)</span><span class="sxs-lookup"><span data-stu-id="b03cf-114">public int fieldCnt2FieldTo(int cnt)</span></span>   | <span data-ttu-id="b03cf-115">マップ フィールドにより参照されているテーブル フィールドを取得します。</span><span class="sxs-lookup"><span data-stu-id="b03cf-115">Retrieves the table field that is referenced by the map field.</span></span> |
| <span data-ttu-id="b03cf-116">public int fieldCnt2FieldFrom(int cnt)</span><span class="sxs-lookup"><span data-stu-id="b03cf-116">public int fieldCnt2FieldFrom(int cnt)</span></span> | <span data-ttu-id="b03cf-117">テーブル フィールドを参照しているマップ フィールドを取得します。</span><span class="sxs-lookup"><span data-stu-id="b03cf-117">Retrieves the map field that is referencing a table field.</span></span>     |

## <a name="method-table"></a><span data-ttu-id="b03cf-118">メソッド table</span><span class="sxs-lookup"><span data-stu-id="b03cf-118">Method table</span></span>

<span data-ttu-id="b03cf-119">マッピングが参照するテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="b03cf-119">Retrieves the table that the mapping references.</span></span>

```xpp
public int table()
```

### <a name="return-value---table"></a><span data-ttu-id="b03cf-120">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="b03cf-120">Return Value - table</span></span>

<span data-ttu-id="b03cf-121">テーブル ID。</span><span class="sxs-lookup"><span data-stu-id="b03cf-121">The table ID.</span></span>

### <a name="remarks---table"></a><span data-ttu-id="b03cf-122">備考 - table</span><span class="sxs-lookup"><span data-stu-id="b03cf-122">Remarks - table</span></span>

<span data-ttu-id="b03cf-123">ツリー ノードをトラバースするのではなく、テーブルのマッピングにアクセスするには、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b03cf-123">Use this method to get to the table mappings, instead of traversing to the tree node.</span></span>

## <a name="method-fieldcnt"></a><span data-ttu-id="b03cf-124">メソッド fieldCnt</span><span class="sxs-lookup"><span data-stu-id="b03cf-124">Method fieldCnt</span></span>

<span data-ttu-id="b03cf-125">テーブル マッピングのフィールドの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="b03cf-125">Retrieves the count of fields in the table mapping.</span></span>

```xpp
public int fieldCnt()
```

### <a name="return-value---fieldcnt"></a><span data-ttu-id="b03cf-126">戻り値 - fieldCnt</span><span class="sxs-lookup"><span data-stu-id="b03cf-126">Return Value - fieldCnt</span></span>

<span data-ttu-id="b03cf-127">カウント。</span><span class="sxs-lookup"><span data-stu-id="b03cf-127">The count.</span></span>

### <a name="remarks---fieldcnt"></a><span data-ttu-id="b03cf-128">備考 - fieldCnt</span><span class="sxs-lookup"><span data-stu-id="b03cf-128">Remarks - fieldCnt</span></span>

<span data-ttu-id="b03cf-129">ツリー ノードをトラバースするのではなく、テーブルのマッピングにアクセスするには、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b03cf-129">Use this method to get to the table mappings, instead of traversing to the tree node.</span></span>

## <a name="method-fieldcnt2fieldto"></a><span data-ttu-id="b03cf-130">メソッド fieldCnt2FieldTo</span><span class="sxs-lookup"><span data-stu-id="b03cf-130">Method fieldCnt2FieldTo</span></span>

<span data-ttu-id="b03cf-131">マップ フィールドにより参照されているテーブル フィールドを取得します。</span><span class="sxs-lookup"><span data-stu-id="b03cf-131">Retrieves the table field that is referenced by the map field.</span></span>

```xpp
public int fieldCnt2FieldTo(int cnt)
```

### <a name="parameters---fieldcnt2fieldto"></a><span data-ttu-id="b03cf-132">パラメーター - fieldCnt2FieldTo</span><span class="sxs-lookup"><span data-stu-id="b03cf-132">Parameters - fieldCnt2FieldTo</span></span>

<span data-ttu-id="b03cf-133">cnt</span><span class="sxs-lookup"><span data-stu-id="b03cf-133">cnt</span></span>  

### <a name="return-value---fieldcnt2fieldto"></a><span data-ttu-id="b03cf-134">戻り値 - fieldCnt2FieldTo</span><span class="sxs-lookup"><span data-stu-id="b03cf-134">Return Value - fieldCnt2FieldTo</span></span>

<span data-ttu-id="b03cf-135">テーブル フィールド ID。</span><span class="sxs-lookup"><span data-stu-id="b03cf-135">The table field ID.</span></span>

### <a name="remarks---fieldcnt2fieldto"></a><span data-ttu-id="b03cf-136">備考 - fieldCnt2FieldTo</span><span class="sxs-lookup"><span data-stu-id="b03cf-136">Remarks - fieldCnt2FieldTo</span></span>

<span data-ttu-id="b03cf-137">ツリー ノードをトラバースするのではなく、テーブルのマッピングにアクセスするには、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b03cf-137">Use this method to get to the table mappings, instead of traversing to the tree node.</span></span>

## <a name="method-fieldcnt2fieldfrom"></a><span data-ttu-id="b03cf-138">メソッド fieldCnt2FieldFrom</span><span class="sxs-lookup"><span data-stu-id="b03cf-138">Method fieldCnt2FieldFrom</span></span>

<span data-ttu-id="b03cf-139">テーブル フィールドを参照しているマップ フィールドを取得します。</span><span class="sxs-lookup"><span data-stu-id="b03cf-139">Retrieves the map field that is referencing a table field.</span></span>

```xpp
public int fieldCnt2FieldFrom(int cnt)
```

### <a name="parameters---fieldcnt2fieldfrom"></a><span data-ttu-id="b03cf-140">パラメーター - fieldCnt2FieldFrom</span><span class="sxs-lookup"><span data-stu-id="b03cf-140">Parameters - fieldCnt2FieldFrom</span></span>

<span data-ttu-id="b03cf-141">cnt</span><span class="sxs-lookup"><span data-stu-id="b03cf-141">cnt</span></span>  

### <a name="return-value---fieldcnt2fieldfrom"></a><span data-ttu-id="b03cf-142">戻り値 - fieldCnt2FieldFrom</span><span class="sxs-lookup"><span data-stu-id="b03cf-142">Return Value - fieldCnt2FieldFrom</span></span>

<span data-ttu-id="b03cf-143">マップ フィールド ID。</span><span class="sxs-lookup"><span data-stu-id="b03cf-143">The map field ID.</span></span>

### <a name="remarks---fieldcnt2fieldfrom"></a><span data-ttu-id="b03cf-144">備考 - fieldCnt2FieldFrom</span><span class="sxs-lookup"><span data-stu-id="b03cf-144">Remarks - fieldCnt2FieldFrom</span></span>

<span data-ttu-id="b03cf-145">ツリー ノードをトラバースするのではなく、テーブルのマッピングにアクセスするには、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b03cf-145">Use this method to get to the table mappings, instead of traversing to the tree node.</span></span>

