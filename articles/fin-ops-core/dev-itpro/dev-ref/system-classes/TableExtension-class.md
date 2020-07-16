---
title: TableExtension クラス
description: このトピックでは、TableExtension クラスについて説明します。
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
ms.openlocfilehash: a37db7c68c8050bb3862d6d9102aaac2a8bc32d8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502791"
---
# <a name="class-tableextension"></a><span data-ttu-id="7f918-103">クラス TableExtension</span><span class="sxs-lookup"><span data-stu-id="7f918-103">Class TableExtension</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class TableExtension extends Object
```

## <a name="remarks"></a><span data-ttu-id="7f918-104">備考</span><span class="sxs-lookup"><span data-stu-id="7f918-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="7f918-105">例</span><span class="sxs-lookup"><span data-stu-id="7f918-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="7f918-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="7f918-106">Methods</span></span>

| <span data-ttu-id="7f918-107">方法</span><span class="sxs-lookup"><span data-stu-id="7f918-107">Method</span></span>                                                    | <span data-ttu-id="7f918-108">説明</span><span class="sxs-lookup"><span data-stu-id="7f918-108">Description</span></span>                                             |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7f918-109">public void new()</span><span class="sxs-lookup"><span data-stu-id="7f918-109">public void new()</span></span>                                         | <span data-ttu-id="7f918-110">TableExtension クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7f918-110">Initializes a new instance of the TableExtension class.</span></span> |
| <span data-ttu-id="7f918-111">public void modifiedField(Common record, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="7f918-111">public void modifiedField(Common record, FieldId fieldId)</span></span> |                                                         |
| <span data-ttu-id="7f918-112">public void defaultRow(Common record)</span><span class="sxs-lookup"><span data-stu-id="7f918-112">public void defaultRow(Common record)</span></span>                     |                                                         |
| <span data-ttu-id="7f918-113">public void defaultField(Common record, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="7f918-113">public void defaultField(Common record, FieldId fieldId)</span></span>  |                                                         |

## <a name="method-new"></a><span data-ttu-id="7f918-114">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7f918-114">Method new</span></span>

<span data-ttu-id="7f918-115">TableExtension クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7f918-115">Initializes a new instance of the TableExtension class.</span></span>

```xpp
public void new()
```

## <a name="method-modifiedfield"></a><span data-ttu-id="7f918-116">メソッド modifiedField</span><span class="sxs-lookup"><span data-stu-id="7f918-116">Method modifiedField</span></span>

```xpp
public void modifiedField(Common record, FieldId fieldId)
```

### <a name="parameters---modifiedfield"></a><span data-ttu-id="7f918-117">パラメーター - modifiedField</span><span class="sxs-lookup"><span data-stu-id="7f918-117">Parameters - modifiedField</span></span>

<span data-ttu-id="7f918-118">記録</span><span class="sxs-lookup"><span data-stu-id="7f918-118">record</span></span>  

<!-- -->

<span data-ttu-id="7f918-119">fieldId</span><span class="sxs-lookup"><span data-stu-id="7f918-119">fieldId</span></span>  

## <a name="method-defaultrow"></a><span data-ttu-id="7f918-120">メソッド defaultRow</span><span class="sxs-lookup"><span data-stu-id="7f918-120">Method defaultRow</span></span>

```xpp
public void defaultRow(Common record)
```

### <a name="parameters---defaultrow"></a><span data-ttu-id="7f918-121">パラメーター - defaultRow</span><span class="sxs-lookup"><span data-stu-id="7f918-121">Parameters - defaultRow</span></span>

<span data-ttu-id="7f918-122">記録</span><span class="sxs-lookup"><span data-stu-id="7f918-122">record</span></span>  

## <a name="method-defaultfield"></a><span data-ttu-id="7f918-123">メソッド defaultField</span><span class="sxs-lookup"><span data-stu-id="7f918-123">Method defaultField</span></span>

```xpp
public void defaultField(Common record, FieldId fieldId)
```

### <a name="parameters---defaultfield"></a><span data-ttu-id="7f918-124">パラメーター - defaultField</span><span class="sxs-lookup"><span data-stu-id="7f918-124">Parameters - defaultField</span></span>

<span data-ttu-id="7f918-125">記録</span><span class="sxs-lookup"><span data-stu-id="7f918-125">record</span></span>  

<!-- -->

<span data-ttu-id="7f918-126">fieldId</span><span class="sxs-lookup"><span data-stu-id="7f918-126">fieldId</span></span>  

