---
title: ValidateFieldValueEventArgs クラス
description: このトピックでは、ValidateFieldValueEventArgs クラスについて説明します。
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
ms.openlocfilehash: 15254286b71ebb062c677d1ed563bfb6524df2ff
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502690"
---
# <a name="class-validatefieldvalueeventargs"></a><span data-ttu-id="73146-103">クラス ValidateFieldValueEventArgs</span><span class="sxs-lookup"><span data-stu-id="73146-103">Class ValidateFieldValueEventArgs</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ValidateFieldValueEventArgs extends ValidateEventArgs
```

## <a name="remarks"></a><span data-ttu-id="73146-104">備考</span><span class="sxs-lookup"><span data-stu-id="73146-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="73146-105">例</span><span class="sxs-lookup"><span data-stu-id="73146-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="73146-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="73146-106">Methods</span></span>

| <span data-ttu-id="73146-107">方法</span><span class="sxs-lookup"><span data-stu-id="73146-107">Method</span></span>                                                         | <span data-ttu-id="73146-108">説明</span><span class="sxs-lookup"><span data-stu-id="73146-108">Description</span></span> |
|----------------------------------------------------------------|-------------|
| <span data-ttu-id="73146-109">public str parmFieldName()</span><span class="sxs-lookup"><span data-stu-id="73146-109">public str parmFieldName()</span></span>                                     |             |
| <span data-ttu-id="73146-110">public int parmArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="73146-110">public int parmArrayIndex()</span></span>                                    |             |
| <span data-ttu-id="73146-111">public void new(str fieldName, int arrayIndex, boolean result)</span><span class="sxs-lookup"><span data-stu-id="73146-111">public void new(str fieldName, int arrayIndex, boolean result)</span></span> |             |

## <a name="method-parmfieldname"></a><span data-ttu-id="73146-112">メソッド parmFieldName</span><span class="sxs-lookup"><span data-stu-id="73146-112">Method parmFieldName</span></span>

```xpp
public str parmFieldName()
```

### <a name="return-value---parmfieldname"></a><span data-ttu-id="73146-113">戻り値 - parmFieldName</span><span class="sxs-lookup"><span data-stu-id="73146-113">Return Value - parmFieldName</span></span>

## <a name="method-parmarrayindex"></a><span data-ttu-id="73146-114">メソッド parmArrayIndex</span><span class="sxs-lookup"><span data-stu-id="73146-114">Method parmArrayIndex</span></span>

```xpp
public int parmArrayIndex()
```

### <a name="return-value---parmarrayindex"></a><span data-ttu-id="73146-115">戻り値 - parmArrayIndex</span><span class="sxs-lookup"><span data-stu-id="73146-115">Return Value - parmArrayIndex</span></span>

## <a name="method-new"></a><span data-ttu-id="73146-116">メソッド new</span><span class="sxs-lookup"><span data-stu-id="73146-116">Method new</span></span>

```xpp
public void new(str fieldName, int arrayIndex, boolean result)
```

### <a name="parameters---new"></a><span data-ttu-id="73146-117">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="73146-117">Parameters - new</span></span>

<span data-ttu-id="73146-118">fieldName</span><span class="sxs-lookup"><span data-stu-id="73146-118">fieldName</span></span>  

<!-- -->

<span data-ttu-id="73146-119">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="73146-119">arrayIndex</span></span>  

<!-- -->

<span data-ttu-id="73146-120">件の結果</span><span class="sxs-lookup"><span data-stu-id="73146-120">result</span></span>  

