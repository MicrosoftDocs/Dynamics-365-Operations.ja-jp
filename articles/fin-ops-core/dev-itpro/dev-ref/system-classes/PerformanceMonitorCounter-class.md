---
title: PerformanceMonitorCounter クラス
description: このトピックでは、PerformanceMonitorCounter クラスについて説明します。
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
ms.openlocfilehash: 4d897956c7f0f5793987cdb40419aa6235f36f7d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502538"
---
# <a name="class-performancemonitorcounter"></a><span data-ttu-id="f7675-103">クラス PerformanceMonitorCounter</span><span class="sxs-lookup"><span data-stu-id="f7675-103">Class PerformanceMonitorCounter</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class PerformanceMonitorCounter extends Object
```

<span data-ttu-id="f7675-104">PerformanceMonitorCounter クラスでは、特定のスナップショットの特定のインスタンスに割り当てられているカウンターを識別します。</span><span class="sxs-lookup"><span data-stu-id="f7675-104">The PerformanceMonitorCounter class identifies a counter that is assigned to a particular instance of a particular snapshot.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7675-105">備考</span><span class="sxs-lookup"><span data-stu-id="f7675-105">Remarks</span></span>

<span data-ttu-id="f7675-106">get メソッドを使用してデータを取得できます。</span><span class="sxs-lookup"><span data-stu-id="f7675-106">The data can be fetched by using the get methods.</span></span>

## <a name="examples"></a><span data-ttu-id="f7675-107">例</span><span class="sxs-lookup"><span data-stu-id="f7675-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f7675-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7675-108">Methods</span></span>

| <span data-ttu-id="f7675-109">方法</span><span class="sxs-lookup"><span data-stu-id="f7675-109">Method</span></span>                 | <span data-ttu-id="f7675-110">説明</span><span class="sxs-lookup"><span data-stu-id="f7675-110">Description</span></span>                                                                                    |
|------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7675-111">public int intData()</span><span class="sxs-lookup"><span data-stu-id="f7675-111">public int intData()</span></span>   |                                                                                                |
| <span data-ttu-id="f7675-112">public str name()</span><span class="sxs-lookup"><span data-stu-id="f7675-112">public str name()</span></span>      |                                                                                                |
| <span data-ttu-id="f7675-113">public Time timeData()</span><span class="sxs-lookup"><span data-stu-id="f7675-113">public Time timeData()</span></span> |                                                                                                |
| <span data-ttu-id="f7675-114">public str toString()</span><span class="sxs-lookup"><span data-stu-id="f7675-114">public str toString()</span></span>  | <span data-ttu-id="f7675-115">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f7675-115">Returns a string that contains the class handle and name, and possibly additional information.</span></span> |

## <a name="method-intdata"></a><span data-ttu-id="f7675-116">メソッド intData</span><span class="sxs-lookup"><span data-stu-id="f7675-116">Method intData</span></span>

```xpp
public int intData()
```

### <a name="return-value---intdata"></a><span data-ttu-id="f7675-117">戻り値 - intData</span><span class="sxs-lookup"><span data-stu-id="f7675-117">Return Value - intData</span></span>

## <a name="method-name"></a><span data-ttu-id="f7675-118">メソッド名</span><span class="sxs-lookup"><span data-stu-id="f7675-118">Method name</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="f7675-119">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="f7675-119">Return Value - name</span></span>

## <a name="method-timedata"></a><span data-ttu-id="f7675-120">メソッド timeData</span><span class="sxs-lookup"><span data-stu-id="f7675-120">Method timeData</span></span>

```xpp
public Time timeData()
```

### <a name="return-value---timedata"></a><span data-ttu-id="f7675-121">戻り値 - timeData</span><span class="sxs-lookup"><span data-stu-id="f7675-121">Return Value - timeData</span></span>

## <a name="method-tostring"></a><span data-ttu-id="f7675-122">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="f7675-122">Method toString</span></span>

<span data-ttu-id="f7675-123">クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f7675-123">Returns a string that contains the class handle and name, and possibly additional information.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="f7675-124">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="f7675-124">Return Value - toString</span></span>

<span data-ttu-id="f7675-125">クラスのテキストの説明。</span><span class="sxs-lookup"><span data-stu-id="f7675-125">A textual description of the class.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="f7675-126">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="f7675-126">Remarks - toString</span></span>

<span data-ttu-id="f7675-127">既定では、ほとんどのクラスは、toString メソッドがクラス ハンドルおよび名前を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f7675-127">By default, for most classes, the toString method returns a string that contains the class handle and name.</span></span> <span data-ttu-id="f7675-128">ただし、一部のクラスでは、追加情報が文字列で返されます。</span><span class="sxs-lookup"><span data-stu-id="f7675-128">However, in some classes additional information is returned in the string.</span></span>

