---
title: LoadAutoCompleteDataEventArgs クラス
description: このトピックでは、LoadAutoCompleteDataEventArgs クラスについて説明します。
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
ms.openlocfilehash: 9b23200afd7f1dd20124238bca457a84a4067ab2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502891"
---
# <a name="class-loadautocompletedataeventargs"></a><span data-ttu-id="a71bf-103">クラス LoadAutoCompleteDataEventArgs</span><span class="sxs-lookup"><span data-stu-id="a71bf-103">Class LoadAutoCompleteDataEventArgs</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class LoadAutoCompleteDataEventArgs extends Object
```

## <a name="remarks"></a><span data-ttu-id="a71bf-104">備考</span><span class="sxs-lookup"><span data-stu-id="a71bf-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="a71bf-105">例</span><span class="sxs-lookup"><span data-stu-id="a71bf-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="a71bf-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="a71bf-106">Methods</span></span>

| <span data-ttu-id="a71bf-107">方法</span><span class="sxs-lookup"><span data-stu-id="a71bf-107">Method</span></span>                                                                                          | <span data-ttu-id="a71bf-108">説明</span><span class="sxs-lookup"><span data-stu-id="a71bf-108">Description</span></span> |
|-------------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="a71bf-109">public AutoCompleteDataMode autoCompleteDataMode(\[AutoCompleteDataMode autoCompleteDataMode\])</span><span class="sxs-lookup"><span data-stu-id="a71bf-109">public AutoCompleteDataMode autoCompleteDataMode(\[AutoCompleteDataMode autoCompleteDataMode\])</span></span> |             |
| <span data-ttu-id="a71bf-110">public boolean canPage(\[boolean canPage\])</span><span class="sxs-lookup"><span data-stu-id="a71bf-110">public boolean canPage(\[boolean canPage\])</span></span>                                                     |             |
| <span data-ttu-id="a71bf-111">public str filterValue()</span><span class="sxs-lookup"><span data-stu-id="a71bf-111">public str filterValue()</span></span>                                                                        |             |
| <span data-ttu-id="a71bf-112">public AnyType lastPagedTag()</span><span class="sxs-lookup"><span data-stu-id="a71bf-112">public AnyType lastPagedTag()</span></span>                                                                   |             |
| <span data-ttu-id="a71bf-113">public FormSegment segment()</span><span class="sxs-lookup"><span data-stu-id="a71bf-113">public FormSegment segment()</span></span>                                                                    |             |
| <span data-ttu-id="a71bf-114">public void addAutoCompleteData(str value, str description, AnyType tag)</span><span class="sxs-lookup"><span data-stu-id="a71bf-114">public void addAutoCompleteData(str value, str description, AnyType tag)</span></span>                        |             |

## <a name="method-autocompletedatamode"></a><span data-ttu-id="a71bf-115">メソッド autoCompleteDataMode</span><span class="sxs-lookup"><span data-stu-id="a71bf-115">Method autoCompleteDataMode</span></span>

```xpp
public AutoCompleteDataMode autoCompleteDataMode([AutoCompleteDataMode autoCompleteDataMode])
```

### <a name="parameters---autocompletedatamode"></a><span data-ttu-id="a71bf-116">パラメーター - autoCompleteDataMode</span><span class="sxs-lookup"><span data-stu-id="a71bf-116">Parameters - autoCompleteDataMode</span></span>

<span data-ttu-id="a71bf-117">autoCompleteDataMode</span><span class="sxs-lookup"><span data-stu-id="a71bf-117">autoCompleteDataMode</span></span>  

### <a name="return-value---autocompletedatamode"></a><span data-ttu-id="a71bf-118">戻り値 - autoCompleteDataMode</span><span class="sxs-lookup"><span data-stu-id="a71bf-118">Return Value - autoCompleteDataMode</span></span>

## <a name="method-canpage"></a><span data-ttu-id="a71bf-119">メソッド canPage</span><span class="sxs-lookup"><span data-stu-id="a71bf-119">Method canPage</span></span>

```xpp
public boolean canPage([boolean canPage])
```

### <a name="parameters---canpage"></a><span data-ttu-id="a71bf-120">パラメーター - canPage</span><span class="sxs-lookup"><span data-stu-id="a71bf-120">Parameters - canPage</span></span>

<span data-ttu-id="a71bf-121">canPage</span><span class="sxs-lookup"><span data-stu-id="a71bf-121">canPage</span></span>  

### <a name="return-value---canpage"></a><span data-ttu-id="a71bf-122">戻り値 - canPage</span><span class="sxs-lookup"><span data-stu-id="a71bf-122">Return Value - canPage</span></span>

## <a name="method-filtervalue"></a><span data-ttu-id="a71bf-123">メソッド filterValue</span><span class="sxs-lookup"><span data-stu-id="a71bf-123">Method filterValue</span></span>

```xpp
public str filterValue()
```

### <a name="return-value---filtervalue"></a><span data-ttu-id="a71bf-124">戻り値 - filterValue</span><span class="sxs-lookup"><span data-stu-id="a71bf-124">Return Value - filterValue</span></span>

## <a name="method-lastpagedtag"></a><span data-ttu-id="a71bf-125">メソッド lastPagedTag</span><span class="sxs-lookup"><span data-stu-id="a71bf-125">Method lastPagedTag</span></span>

```xpp
public AnyType lastPagedTag()
```

### <a name="return-value---lastpagedtag"></a><span data-ttu-id="a71bf-126">戻り値 - lastPagedTag</span><span class="sxs-lookup"><span data-stu-id="a71bf-126">Return Value - lastPagedTag</span></span>

## <a name="method-segment"></a><span data-ttu-id="a71bf-127">メソッド segment</span><span class="sxs-lookup"><span data-stu-id="a71bf-127">Method segment</span></span>

```xpp
public FormSegment segment()
```

### <a name="return-value---segment"></a><span data-ttu-id="a71bf-128">戻り値 - segment</span><span class="sxs-lookup"><span data-stu-id="a71bf-128">Return Value - segment</span></span>

## <a name="method-addautocompletedata"></a><span data-ttu-id="a71bf-129">メソッド addAutoCompleteData</span><span class="sxs-lookup"><span data-stu-id="a71bf-129">Method addAutoCompleteData</span></span>

```xpp
public void addAutoCompleteData(str value, str description, AnyType tag)
```

### <a name="parameters---addautocompletedata"></a><span data-ttu-id="a71bf-130">パラメーター - addAutoCompleteData</span><span class="sxs-lookup"><span data-stu-id="a71bf-130">Parameters - addAutoCompleteData</span></span>

<span data-ttu-id="a71bf-131">値</span><span class="sxs-lookup"><span data-stu-id="a71bf-131">value</span></span>  

<!-- -->

<span data-ttu-id="a71bf-132">説明</span><span class="sxs-lookup"><span data-stu-id="a71bf-132">description</span></span>  

<!-- -->

<span data-ttu-id="a71bf-133">タグ</span><span class="sxs-lookup"><span data-stu-id="a71bf-133">tag</span></span>  

