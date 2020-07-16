---
title: IISStringList クラス
description: このトピックでは、IISStringList クラスについて説明します。
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
ms.openlocfilehash: 087be3b8f22903ca6175d197e2d081f30d725e69
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502904"
---
# <a name="class-iisstringlist"></a><span data-ttu-id="1ad21-103">クラス IISStringList</span><span class="sxs-lookup"><span data-stu-id="1ad21-103">Class IISStringList</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class IISStringList extends Object
```

<span data-ttu-id="1ad21-104">IISStringList クラスは、インターネット インフォメーション サービス (IIS) によって提供される StringList オブジェクトをラップします。</span><span class="sxs-lookup"><span data-stu-id="1ad21-104">The IISStringList class wraps the StringList object that is offered by Internet Information Services (IIS).</span></span>

## <a name="remarks"></a><span data-ttu-id="1ad21-105">備考</span><span class="sxs-lookup"><span data-stu-id="1ad21-105">Remarks</span></span>

<span data-ttu-id="1ad21-106">IISStringList クラスのメソッドと、IIS によって提供される StringList オブジェクトのメソッドとの間には、1 対 1 の接続があります。</span><span class="sxs-lookup"><span data-stu-id="1ad21-106">There is a one-to-one connection between the methods of the IISStringList class and the methods of the StringList object that is offered by IIS.</span></span> <span data-ttu-id="1ad21-107">したがって、IISStringList クラスのメソッドの詳細については、IIS の Microsoft ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1ad21-107">Therefore, for more information about the methods of the IISStringList class, see the Microsoft documentation for IIS.</span></span> <span data-ttu-id="1ad21-108">IISStringList クラスの使用は、IIS がインターネット コネクタによって実行されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="1ad21-108">Use of the IISStringList class is valid only when code is run by the Internet Connector under IIS.</span></span>

## <a name="examples"></a><span data-ttu-id="1ad21-109">例</span><span class="sxs-lookup"><span data-stu-id="1ad21-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="1ad21-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="1ad21-110">Methods</span></span>

| <span data-ttu-id="1ad21-111">方法</span><span class="sxs-lookup"><span data-stu-id="1ad21-111">Method</span></span>                           | <span data-ttu-id="1ad21-112">説明</span><span class="sxs-lookup"><span data-stu-id="1ad21-112">Description</span></span>                                     |
|----------------------------------|-------------------------------------------------|
| <span data-ttu-id="1ad21-113">public int count()</span><span class="sxs-lookup"><span data-stu-id="1ad21-113">public int count()</span></span>               |                                                 |
| <span data-ttu-id="1ad21-114">public COMEnum2Variant getEnum()</span><span class="sxs-lookup"><span data-stu-id="1ad21-114">public COMEnum2Variant getEnum()</span></span> |                                                 |
| <span data-ttu-id="1ad21-115">public ComInterface interface()</span><span class="sxs-lookup"><span data-stu-id="1ad21-115">public ComInterface interface()</span></span>  |                                                 |
| <span data-ttu-id="1ad21-116">public str item(\[str item\])</span><span class="sxs-lookup"><span data-stu-id="1ad21-116">public str item(\[str item\])</span></span>    |                                                 |
| <span data-ttu-id="1ad21-117">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="1ad21-117">public void finalize()</span></span>           |                                                 |
| <span data-ttu-id="1ad21-118">public void new(COM stringList)</span><span class="sxs-lookup"><span data-stu-id="1ad21-118">public void new(COM stringList)</span></span>  | <span data-ttu-id="1ad21-119">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="1ad21-119">Initializes a new instance of the Object class.</span></span> |

## <a name="method-count"></a><span data-ttu-id="1ad21-120">メソッド count</span><span class="sxs-lookup"><span data-stu-id="1ad21-120">Method count</span></span>

```xpp
public int count()
```

### <a name="return-value---count"></a><span data-ttu-id="1ad21-121">戻り値 - count</span><span class="sxs-lookup"><span data-stu-id="1ad21-121">Return Value - count</span></span>

## <a name="method-getenum"></a><span data-ttu-id="1ad21-122">メソッド getEnum</span><span class="sxs-lookup"><span data-stu-id="1ad21-122">Method getEnum</span></span>

```xpp
public COMEnum2Variant getEnum()
```

### <a name="return-value---getenum"></a><span data-ttu-id="1ad21-123">戻り値 - getEnum</span><span class="sxs-lookup"><span data-stu-id="1ad21-123">Return Value - getEnum</span></span>

## <a name="method-interface"></a><span data-ttu-id="1ad21-124">メソッド interface</span><span class="sxs-lookup"><span data-stu-id="1ad21-124">Method interface</span></span>

```xpp
public ComInterface interface()
```

### <a name="return-value---interface"></a><span data-ttu-id="1ad21-125">戻り値 - interface</span><span class="sxs-lookup"><span data-stu-id="1ad21-125">Return Value - interface</span></span>

## <a name="method-item"></a><span data-ttu-id="1ad21-126">メソッド item</span><span class="sxs-lookup"><span data-stu-id="1ad21-126">Method item</span></span>

```xpp
public str item([str item])
```

### <a name="parameters---item"></a><span data-ttu-id="1ad21-127">パラメーター - item</span><span class="sxs-lookup"><span data-stu-id="1ad21-127">Parameters - item</span></span>

<span data-ttu-id="1ad21-128">品目</span><span class="sxs-lookup"><span data-stu-id="1ad21-128">item</span></span>  

### <a name="return-value---item"></a><span data-ttu-id="1ad21-129">戻り値 - item</span><span class="sxs-lookup"><span data-stu-id="1ad21-129">Return Value - item</span></span>

## <a name="method-finalize"></a><span data-ttu-id="1ad21-130">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="1ad21-130">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="1ad21-131">メソッド new</span><span class="sxs-lookup"><span data-stu-id="1ad21-131">Method new</span></span>

<span data-ttu-id="1ad21-132">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="1ad21-132">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(COM stringList)
```

### <a name="parameters---new"></a><span data-ttu-id="1ad21-133">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="1ad21-133">Parameters - new</span></span>

<span data-ttu-id="1ad21-134">stringList</span><span class="sxs-lookup"><span data-stu-id="1ad21-134">stringList</span></span>  

