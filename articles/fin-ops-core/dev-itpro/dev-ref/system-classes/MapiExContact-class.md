---
title: MapiExContact クラス
description: このトピックでは、MapiExContact クラスについて説明します。
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
ms.openlocfilehash: ae1f772eca64fb0ce21eb97bb769f9ee912313c1
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502584"
---
# <a name="class-mapiexcontact"></a><span data-ttu-id="b9b97-103">クラス MapiExContact</span><span class="sxs-lookup"><span data-stu-id="b9b97-103">Class MapiExContact</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class MapiExContact extends MapiExMessage
```

## <a name="remarks"></a><span data-ttu-id="b9b97-104">備考</span><span class="sxs-lookup"><span data-stu-id="b9b97-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="b9b97-105">例</span><span class="sxs-lookup"><span data-stu-id="b9b97-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b9b97-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="b9b97-106">Methods</span></span>

| <span data-ttu-id="b9b97-107">方法</span><span class="sxs-lookup"><span data-stu-id="b9b97-107">Method</span></span>                            | <span data-ttu-id="b9b97-108">説明</span><span class="sxs-lookup"><span data-stu-id="b9b97-108">Description</span></span>                                            |
|-----------------------------------|--------------------------------------------------------|
| <span data-ttu-id="b9b97-109">public str entryId()</span><span class="sxs-lookup"><span data-stu-id="b9b97-109">public str entryId()</span></span>              |                                                        |
| <span data-ttu-id="b9b97-110">public str getBody()</span><span class="sxs-lookup"><span data-stu-id="b9b97-110">public str getBody()</span></span>              |                                                        |
| <span data-ttu-id="b9b97-111">public str getEmail1()</span><span class="sxs-lookup"><span data-stu-id="b9b97-111">public str getEmail1()</span></span>            |                                                        |
| <span data-ttu-id="b9b97-112">public str getEmail1DisplayName()</span><span class="sxs-lookup"><span data-stu-id="b9b97-112">public str getEmail1DisplayName()</span></span> |                                                        |
| <span data-ttu-id="b9b97-113">public str getEmail1Type()</span><span class="sxs-lookup"><span data-stu-id="b9b97-113">public str getEmail1Type()</span></span>        |                                                        |
| <span data-ttu-id="b9b97-114">public str getEmail2()</span><span class="sxs-lookup"><span data-stu-id="b9b97-114">public str getEmail2()</span></span>            |                                                        |
| <span data-ttu-id="b9b97-115">public str getEmail2DisplayName()</span><span class="sxs-lookup"><span data-stu-id="b9b97-115">public str getEmail2DisplayName()</span></span> |                                                        |
| <span data-ttu-id="b9b97-116">public str getEmail2Type()</span><span class="sxs-lookup"><span data-stu-id="b9b97-116">public str getEmail2Type()</span></span>        |                                                        |
| <span data-ttu-id="b9b97-117">public str getEmail3()</span><span class="sxs-lookup"><span data-stu-id="b9b97-117">public str getEmail3()</span></span>            |                                                        |
| <span data-ttu-id="b9b97-118">public str getEmail3DisplayName()</span><span class="sxs-lookup"><span data-stu-id="b9b97-118">public str getEmail3DisplayName()</span></span> |                                                        |
| <span data-ttu-id="b9b97-119">public str getEmail3Type()</span><span class="sxs-lookup"><span data-stu-id="b9b97-119">public str getEmail3Type()</span></span>        |                                                        |
| <span data-ttu-id="b9b97-120">public str getIMAddress()</span><span class="sxs-lookup"><span data-stu-id="b9b97-120">public str getIMAddress()</span></span>         |                                                        |
| <span data-ttu-id="b9b97-121">public boolean save()</span><span class="sxs-lookup"><span data-stu-id="b9b97-121">public boolean save()</span></span>             |                                                        |
| <span data-ttu-id="b9b97-122">public boolean setBody(str body)</span><span class="sxs-lookup"><span data-stu-id="b9b97-122">public boolean setBody(str body)</span></span>  |                                                        |
| <span data-ttu-id="b9b97-123">public void close()</span><span class="sxs-lookup"><span data-stu-id="b9b97-123">public void close()</span></span>               |                                                        |
| <span data-ttu-id="b9b97-124">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="b9b97-124">public void finalize()</span></span>            |                                                        |
| <span data-ttu-id="b9b97-125">public void new()</span><span class="sxs-lookup"><span data-stu-id="b9b97-125">public void new()</span></span>                 | <span data-ttu-id="b9b97-126">MapiExContact クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b9b97-126">Initializes a new instance of the MapiExContact class.</span></span> |

## <a name="method-entryid"></a><span data-ttu-id="b9b97-127">メソッド entryId</span><span class="sxs-lookup"><span data-stu-id="b9b97-127">Method entryId</span></span>

```xpp
public str entryId()
```

### <a name="return-value---entryid"></a><span data-ttu-id="b9b97-128">戻り値 - entryId</span><span class="sxs-lookup"><span data-stu-id="b9b97-128">Return Value - entryId</span></span>

## <a name="method-getbody"></a><span data-ttu-id="b9b97-129">メソッド getBody</span><span class="sxs-lookup"><span data-stu-id="b9b97-129">Method getBody</span></span>

```xpp
public str getBody()
```

### <a name="return-value---getbody"></a><span data-ttu-id="b9b97-130">戻り値 - getBody</span><span class="sxs-lookup"><span data-stu-id="b9b97-130">Return Value - getBody</span></span>

## <a name="method-getemail1"></a><span data-ttu-id="b9b97-131">メソッド getEmail1</span><span class="sxs-lookup"><span data-stu-id="b9b97-131">Method getEmail1</span></span>

```xpp
public str getEmail1()
```

### <a name="return-value---getemail1"></a><span data-ttu-id="b9b97-132">戻り値 - getEmail1</span><span class="sxs-lookup"><span data-stu-id="b9b97-132">Return Value - getEmail1</span></span>

## <a name="method-getemail1displayname"></a><span data-ttu-id="b9b97-133">メソッド getEmail1DisplayName</span><span class="sxs-lookup"><span data-stu-id="b9b97-133">Method getEmail1DisplayName</span></span>

```xpp
public str getEmail1DisplayName()
```

### <a name="return-value---getemail1displayname"></a><span data-ttu-id="b9b97-134">戻り値 - getEmail1DisplayName</span><span class="sxs-lookup"><span data-stu-id="b9b97-134">Return Value - getEmail1DisplayName</span></span>

## <a name="method-getemail1type"></a><span data-ttu-id="b9b97-135">メソッド getEmail1Type</span><span class="sxs-lookup"><span data-stu-id="b9b97-135">Method getEmail1Type</span></span>

```xpp
public str getEmail1Type()
```

### <a name="return-value---getemail1type"></a><span data-ttu-id="b9b97-136">戻り値 - getEmail1Type</span><span class="sxs-lookup"><span data-stu-id="b9b97-136">Return Value - getEmail1Type</span></span>

## <a name="method-getemail2"></a><span data-ttu-id="b9b97-137">メソッド getEmail2</span><span class="sxs-lookup"><span data-stu-id="b9b97-137">Method getEmail2</span></span>

```xpp
public str getEmail2()
```

### <a name="return-value---getemail2"></a><span data-ttu-id="b9b97-138">戻り値 - getEmail2</span><span class="sxs-lookup"><span data-stu-id="b9b97-138">Return Value - getEmail2</span></span>

## <a name="method-getemail2displayname"></a><span data-ttu-id="b9b97-139">メソッド getEmail2DisplayName</span><span class="sxs-lookup"><span data-stu-id="b9b97-139">Method getEmail2DisplayName</span></span>

```xpp
public str getEmail2DisplayName()
```

### <a name="return-value---getemail2displayname"></a><span data-ttu-id="b9b97-140">戻り値 - getEmail2DisplayName</span><span class="sxs-lookup"><span data-stu-id="b9b97-140">Return Value - getEmail2DisplayName</span></span>

## <a name="method-getemail2type"></a><span data-ttu-id="b9b97-141">メソッド getEmail2Type</span><span class="sxs-lookup"><span data-stu-id="b9b97-141">Method getEmail2Type</span></span>

```xpp
public str getEmail2Type()
```

### <a name="return-value---getemail2type"></a><span data-ttu-id="b9b97-142">戻り値 - getEmail2Type</span><span class="sxs-lookup"><span data-stu-id="b9b97-142">Return Value - getEmail2Type</span></span>

## <a name="method-getemail3"></a><span data-ttu-id="b9b97-143">メソッド getEmail3</span><span class="sxs-lookup"><span data-stu-id="b9b97-143">Method getEmail3</span></span>

```xpp
public str getEmail3()
```

### <a name="return-value---getemail3"></a><span data-ttu-id="b9b97-144">戻り値 - getEmail3</span><span class="sxs-lookup"><span data-stu-id="b9b97-144">Return Value - getEmail3</span></span>

## <a name="method-getemail3displayname"></a><span data-ttu-id="b9b97-145">メソッド getEmail3DisplayName</span><span class="sxs-lookup"><span data-stu-id="b9b97-145">Method getEmail3DisplayName</span></span>

```xpp
public str getEmail3DisplayName()
```

### <a name="return-value---getemail3displayname"></a><span data-ttu-id="b9b97-146">戻り値 - getEmail3DisplayName</span><span class="sxs-lookup"><span data-stu-id="b9b97-146">Return Value - getEmail3DisplayName</span></span>

## <a name="method-getemail3type"></a><span data-ttu-id="b9b97-147">メソッド getEmail3Type</span><span class="sxs-lookup"><span data-stu-id="b9b97-147">Method getEmail3Type</span></span>

```xpp
public str getEmail3Type()
```

### <a name="return-value---getemail3type"></a><span data-ttu-id="b9b97-148">戻り値 - getEmail3Type</span><span class="sxs-lookup"><span data-stu-id="b9b97-148">Return Value - getEmail3Type</span></span>

## <a name="method-getimaddress"></a><span data-ttu-id="b9b97-149">メソッド getIMAddress</span><span class="sxs-lookup"><span data-stu-id="b9b97-149">Method getIMAddress</span></span>

```xpp
public str getIMAddress()
```

### <a name="return-value---getimaddress"></a><span data-ttu-id="b9b97-150">戻り値 - getIMAddress</span><span class="sxs-lookup"><span data-stu-id="b9b97-150">Return Value - getIMAddress</span></span>

## <a name="method-save"></a><span data-ttu-id="b9b97-151">メソッド save</span><span class="sxs-lookup"><span data-stu-id="b9b97-151">Method save</span></span>

```xpp
public boolean save()
```

### <a name="return-value---save"></a><span data-ttu-id="b9b97-152">戻り値 - save</span><span class="sxs-lookup"><span data-stu-id="b9b97-152">Return Value - save</span></span>

## <a name="method-setbody"></a><span data-ttu-id="b9b97-153">メソッド setBody</span><span class="sxs-lookup"><span data-stu-id="b9b97-153">Method setBody</span></span>

```xpp
public boolean setBody(str body)
```

### <a name="parameters---setbody"></a><span data-ttu-id="b9b97-154">パラメーター - setBody</span><span class="sxs-lookup"><span data-stu-id="b9b97-154">Parameters - setBody</span></span>

<span data-ttu-id="b9b97-155">body</span><span class="sxs-lookup"><span data-stu-id="b9b97-155">body</span></span>  

### <a name="return-value---setbody"></a><span data-ttu-id="b9b97-156">戻り値 - setBody</span><span class="sxs-lookup"><span data-stu-id="b9b97-156">Return Value - setBody</span></span>

## <a name="method-close"></a><span data-ttu-id="b9b97-157">メソッド close</span><span class="sxs-lookup"><span data-stu-id="b9b97-157">Method close</span></span>

```xpp
public void close()
```

## <a name="method-finalize"></a><span data-ttu-id="b9b97-158">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="b9b97-158">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="b9b97-159">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b9b97-159">Method new</span></span>

<span data-ttu-id="b9b97-160">MapiExContact クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b9b97-160">Initializes a new instance of the MapiExContact class.</span></span>

```xpp
public void new()
```

