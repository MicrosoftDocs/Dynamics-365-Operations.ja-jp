---
title: FormDataRow クラス
description: このトピックでは、FormDataRow クラスについて説明します。
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
ms.openlocfilehash: f0a64163457c4184da3364460200e6c48dd25a4e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502626"
---
# <a name="class-formdatarow"></a><span data-ttu-id="f9dc5-103">クラス FormDataRow</span><span class="sxs-lookup"><span data-stu-id="f9dc5-103">Class FormDataRow</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormDataRow extends Object
```

## <a name="remarks"></a><span data-ttu-id="f9dc5-104">備考</span><span class="sxs-lookup"><span data-stu-id="f9dc5-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="f9dc5-105">例</span><span class="sxs-lookup"><span data-stu-id="f9dc5-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f9dc5-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="f9dc5-106">Methods</span></span>

| <span data-ttu-id="f9dc5-107">方法</span><span class="sxs-lookup"><span data-stu-id="f9dc5-107">Method</span></span>                                                                       | <span data-ttu-id="f9dc5-108">説明</span><span class="sxs-lookup"><span data-stu-id="f9dc5-108">Description</span></span>                                          |
|------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9dc5-109">public Object associatedObject(\[Object value\], \[boolean notifyDetached\])</span><span class="sxs-lookup"><span data-stu-id="f9dc5-109">public Object associatedObject(\[Object value\], \[boolean notifyDetached\])</span></span> |                                                      |
| <span data-ttu-id="f9dc5-110">public boolean isDetached()</span><span class="sxs-lookup"><span data-stu-id="f9dc5-110">public boolean isDetached()</span></span>                                                  |                                                      |
| <span data-ttu-id="f9dc5-111">public int rowIndex()</span><span class="sxs-lookup"><span data-stu-id="f9dc5-111">public int rowIndex()</span></span>                                                        |                                                      |
| <span data-ttu-id="f9dc5-112">private void new()</span><span class="sxs-lookup"><span data-stu-id="f9dc5-112">private void new()</span></span>                                                           | <span data-ttu-id="f9dc5-113">FormDataRow クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f9dc5-113">Initializes a new instance of the FormDataRow class.</span></span> |
| <span data-ttu-id="f9dc5-114">public void clearAssociatedObject()</span><span class="sxs-lookup"><span data-stu-id="f9dc5-114">public void clearAssociatedObject()</span></span>                                          |                                                      |

## <a name="method-associatedobject"></a><span data-ttu-id="f9dc5-115">メソッド associatedObject</span><span class="sxs-lookup"><span data-stu-id="f9dc5-115">Method associatedObject</span></span>

```xpp
public Object associatedObject([Object value], [boolean notifyDetached])
```

### <a name="parameters---associatedobject"></a><span data-ttu-id="f9dc5-116">パラメーター - associatedObject</span><span class="sxs-lookup"><span data-stu-id="f9dc5-116">Parameters - associatedObject</span></span>

<span data-ttu-id="f9dc5-117">値</span><span class="sxs-lookup"><span data-stu-id="f9dc5-117">value</span></span>  

<!-- -->

<span data-ttu-id="f9dc5-118">notifyDetached</span><span class="sxs-lookup"><span data-stu-id="f9dc5-118">notifyDetached</span></span>  

### <a name="return-value---associatedobject"></a><span data-ttu-id="f9dc5-119">戻り値 - associatedObject</span><span class="sxs-lookup"><span data-stu-id="f9dc5-119">Return Value - associatedObject</span></span>

## <a name="method-isdetached"></a><span data-ttu-id="f9dc5-120">メソッド isDetached</span><span class="sxs-lookup"><span data-stu-id="f9dc5-120">Method isDetached</span></span>

```xpp
public boolean isDetached()
```

### <a name="return-value---isdetached"></a><span data-ttu-id="f9dc5-121">戻り値 - isDetached</span><span class="sxs-lookup"><span data-stu-id="f9dc5-121">Return Value - isDetached</span></span>

## <a name="method-rowindex"></a><span data-ttu-id="f9dc5-122">メソッド rowIndex</span><span class="sxs-lookup"><span data-stu-id="f9dc5-122">Method rowIndex</span></span>

```xpp
public int rowIndex()
```

### <a name="return-value---rowindex"></a><span data-ttu-id="f9dc5-123">戻り値 - rowIndex</span><span class="sxs-lookup"><span data-stu-id="f9dc5-123">Return Value - rowIndex</span></span>

## <a name="method-new"></a><span data-ttu-id="f9dc5-124">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f9dc5-124">Method new</span></span>

<span data-ttu-id="f9dc5-125">FormDataRow クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f9dc5-125">Initializes a new instance of the FormDataRow class.</span></span>

```xpp
private void new()
```

## <a name="method-clearassociatedobject"></a><span data-ttu-id="f9dc5-126">メソッド clearAssociatedObject</span><span class="sxs-lookup"><span data-stu-id="f9dc5-126">Method clearAssociatedObject</span></span>

```xpp
public void clearAssociatedObject()
```

