---
title: PresenceInfo クラス
description: このトピックでは、PresenceInfo クラスについて説明します。
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
ms.openlocfilehash: 70bcf43b42a315f3ae5254fc3b492ae3a7983994
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502540"
---
# <a name="class-presenceinfo"></a><span data-ttu-id="2c584-103">クラス PresenceInfo</span><span class="sxs-lookup"><span data-stu-id="2c584-103">Class PresenceInfo</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class PresenceInfo extends Object
```

## <a name="remarks"></a><span data-ttu-id="2c584-104">備考</span><span class="sxs-lookup"><span data-stu-id="2c584-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="2c584-105">例</span><span class="sxs-lookup"><span data-stu-id="2c584-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="2c584-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="2c584-106">Methods</span></span>

| <span data-ttu-id="2c584-107">方法</span><span class="sxs-lookup"><span data-stu-id="2c584-107">Method</span></span>                                                                | <span data-ttu-id="2c584-108">説明</span><span class="sxs-lookup"><span data-stu-id="2c584-108">Description</span></span>                                           |
|-----------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="2c584-109">public str contactName(\[str contactName\])</span><span class="sxs-lookup"><span data-stu-id="2c584-109">public str contactName(\[str contactName\])</span></span>                           |                                                       |
| <span data-ttu-id="2c584-110">public str emailAddress(int index)</span><span class="sxs-lookup"><span data-stu-id="2c584-110">public str emailAddress(int index)</span></span>                                    |                                                       |
| <span data-ttu-id="2c584-111">public str emailAlias(int index)</span><span class="sxs-lookup"><span data-stu-id="2c584-111">public str emailAlias(int index)</span></span>                                      |                                                       |
| <span data-ttu-id="2c584-112">public int emailCount()</span><span class="sxs-lookup"><span data-stu-id="2c584-112">public int emailCount()</span></span>                                               |                                                       |
| <span data-ttu-id="2c584-113">public str phoneAlias(int index)</span><span class="sxs-lookup"><span data-stu-id="2c584-113">public str phoneAlias(int index)</span></span>                                      |                                                       |
| <span data-ttu-id="2c584-114">public int phoneCount()</span><span class="sxs-lookup"><span data-stu-id="2c584-114">public int phoneCount()</span></span>                                               |                                                       |
| <span data-ttu-id="2c584-115">public str phoneNumber(int index)</span><span class="sxs-lookup"><span data-stu-id="2c584-115">public str phoneNumber(int index)</span></span>                                     |                                                       |
| <span data-ttu-id="2c584-116">public str sipAddress(\[str sipAddress\])</span><span class="sxs-lookup"><span data-stu-id="2c584-116">public str sipAddress(\[str sipAddress\])</span></span>                             |                                                       |
| <span data-ttu-id="2c584-117">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="2c584-117">public void finalize()</span></span>                                                |                                                       |
| <span data-ttu-id="2c584-118">public void new()</span><span class="sxs-lookup"><span data-stu-id="2c584-118">public void new()</span></span>                                                     | <span data-ttu-id="2c584-119">PresenceInfo クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="2c584-119">Initializes a new instance of the PresenceInfo class.</span></span> |
| <span data-ttu-id="2c584-120">public void addEmailAddress(\[str emailAlias\], \[str emailAddress\])</span><span class="sxs-lookup"><span data-stu-id="2c584-120">public void addEmailAddress(\[str emailAlias\], \[str emailAddress\])</span></span> |                                                       |
| <span data-ttu-id="2c584-121">public void addPhoneNumber(\[str phoneAlias\], \[str phoneNumber\])</span><span class="sxs-lookup"><span data-stu-id="2c584-121">public void addPhoneNumber(\[str phoneAlias\], \[str phoneNumber\])</span></span>   |                                                       |

## <a name="method-contactname"></a><span data-ttu-id="2c584-122">メソッド contactName</span><span class="sxs-lookup"><span data-stu-id="2c584-122">Method contactName</span></span>

```xpp
public str contactName([str contactName])
```

### <a name="parameters---contactname"></a><span data-ttu-id="2c584-123">パラメーター - contactName</span><span class="sxs-lookup"><span data-stu-id="2c584-123">Parameters - contactName</span></span>

<span data-ttu-id="2c584-124">contactName</span><span class="sxs-lookup"><span data-stu-id="2c584-124">contactName</span></span>  

### <a name="return-value---contactname"></a><span data-ttu-id="2c584-125">戻り値 - contactName</span><span class="sxs-lookup"><span data-stu-id="2c584-125">Return Value - contactName</span></span>

## <a name="method-emailaddress"></a><span data-ttu-id="2c584-126">メソッド emailAddress</span><span class="sxs-lookup"><span data-stu-id="2c584-126">Method emailAddress</span></span>

```xpp
public str emailAddress(int index)
```

### <a name="parameters---emailaddress"></a><span data-ttu-id="2c584-127">パラメーター - emailAddress</span><span class="sxs-lookup"><span data-stu-id="2c584-127">Parameters - emailAddress</span></span>

<span data-ttu-id="2c584-128">指数</span><span class="sxs-lookup"><span data-stu-id="2c584-128">index</span></span>  

### <a name="return-value---emailaddress"></a><span data-ttu-id="2c584-129">戻り値 - emailAddress</span><span class="sxs-lookup"><span data-stu-id="2c584-129">Return Value - emailAddress</span></span>

## <a name="method-emailalias"></a><span data-ttu-id="2c584-130">メソッド emailAlias</span><span class="sxs-lookup"><span data-stu-id="2c584-130">Method emailAlias</span></span>

```xpp
public str emailAlias(int index)
```

### <a name="parameters---emailalias"></a><span data-ttu-id="2c584-131">パラメーター - emailAlias</span><span class="sxs-lookup"><span data-stu-id="2c584-131">Parameters - emailAlias</span></span>

<span data-ttu-id="2c584-132">指数</span><span class="sxs-lookup"><span data-stu-id="2c584-132">index</span></span>  

### <a name="return-value---emailalias"></a><span data-ttu-id="2c584-133">戻り値 - emailAlias</span><span class="sxs-lookup"><span data-stu-id="2c584-133">Return Value - emailAlias</span></span>

## <a name="method-emailcount"></a><span data-ttu-id="2c584-134">メソッド emailCount</span><span class="sxs-lookup"><span data-stu-id="2c584-134">Method emailCount</span></span>

```xpp
public int emailCount()
```

### <a name="return-value---emailcount"></a><span data-ttu-id="2c584-135">戻り値 - emailCount</span><span class="sxs-lookup"><span data-stu-id="2c584-135">Return Value - emailCount</span></span>

## <a name="method-phonealias"></a><span data-ttu-id="2c584-136">メソッド phoneAlias</span><span class="sxs-lookup"><span data-stu-id="2c584-136">Method phoneAlias</span></span>

```xpp
public str phoneAlias(int index)
```

### <a name="parameters---phonealias"></a><span data-ttu-id="2c584-137">パラメーター - phoneAlias</span><span class="sxs-lookup"><span data-stu-id="2c584-137">Parameters - phoneAlias</span></span>

<span data-ttu-id="2c584-138">指数</span><span class="sxs-lookup"><span data-stu-id="2c584-138">index</span></span>  

### <a name="return-value---phonealias"></a><span data-ttu-id="2c584-139">戻り値 - phoneAlias</span><span class="sxs-lookup"><span data-stu-id="2c584-139">Return Value - phoneAlias</span></span>

## <a name="method-phonecount"></a><span data-ttu-id="2c584-140">メソッド phoneCount</span><span class="sxs-lookup"><span data-stu-id="2c584-140">Method phoneCount</span></span>

```xpp
public int phoneCount()
```

### <a name="return-value---phonecount"></a><span data-ttu-id="2c584-141">戻り値 - phoneCount</span><span class="sxs-lookup"><span data-stu-id="2c584-141">Return Value - phoneCount</span></span>

## <a name="method-phonenumber"></a><span data-ttu-id="2c584-142">メソッド phoneNumber</span><span class="sxs-lookup"><span data-stu-id="2c584-142">Method phoneNumber</span></span>

```xpp
public str phoneNumber(int index)
```

### <a name="parameters---phonenumber"></a><span data-ttu-id="2c584-143">パラメーター - phoneNumber</span><span class="sxs-lookup"><span data-stu-id="2c584-143">Parameters - phoneNumber</span></span>

<span data-ttu-id="2c584-144">指数</span><span class="sxs-lookup"><span data-stu-id="2c584-144">index</span></span>  

### <a name="return-value---phonenumber"></a><span data-ttu-id="2c584-145">戻り値 - phoneNumber</span><span class="sxs-lookup"><span data-stu-id="2c584-145">Return Value - phoneNumber</span></span>

## <a name="method-sipaddress"></a><span data-ttu-id="2c584-146">メソッド sipAddress</span><span class="sxs-lookup"><span data-stu-id="2c584-146">Method sipAddress</span></span>

```xpp
public str sipAddress([str sipAddress])
```

### <a name="parameters---sipaddress"></a><span data-ttu-id="2c584-147">パラメーター - sipAddress</span><span class="sxs-lookup"><span data-stu-id="2c584-147">Parameters - sipAddress</span></span>

<span data-ttu-id="2c584-148">sipAddress</span><span class="sxs-lookup"><span data-stu-id="2c584-148">sipAddress</span></span>  

### <a name="return-value---sipaddress"></a><span data-ttu-id="2c584-149">戻り値 - sipAddress</span><span class="sxs-lookup"><span data-stu-id="2c584-149">Return Value - sipAddress</span></span>

## <a name="method-finalize"></a><span data-ttu-id="2c584-150">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="2c584-150">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="2c584-151">メソッド new</span><span class="sxs-lookup"><span data-stu-id="2c584-151">Method new</span></span>

<span data-ttu-id="2c584-152">PresenceInfo クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="2c584-152">Initializes a new instance of the PresenceInfo class.</span></span>

```xpp
public void new()
```

## <a name="method-addemailaddress"></a><span data-ttu-id="2c584-153">メソッド addEmailAddress</span><span class="sxs-lookup"><span data-stu-id="2c584-153">Method addEmailAddress</span></span>

```xpp
public void addEmailAddress([str emailAlias], [str emailAddress])
```

### <a name="parameters---addemailaddress"></a><span data-ttu-id="2c584-154">パラメーター - addEmailAddress</span><span class="sxs-lookup"><span data-stu-id="2c584-154">Parameters - addEmailAddress</span></span>

<span data-ttu-id="2c584-155">emailAlias</span><span class="sxs-lookup"><span data-stu-id="2c584-155">emailAlias</span></span>  

<!-- -->

<span data-ttu-id="2c584-156">emailAddress</span><span class="sxs-lookup"><span data-stu-id="2c584-156">emailAddress</span></span>  

## <a name="method-addphonenumber"></a><span data-ttu-id="2c584-157">メソッド addPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="2c584-157">Method addPhoneNumber</span></span>

```xpp
public void addPhoneNumber([str phoneAlias], [str phoneNumber])
```

### <a name="parameters---addphonenumber"></a><span data-ttu-id="2c584-158">パラメーター - addPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="2c584-158">Parameters - addPhoneNumber</span></span>

<span data-ttu-id="2c584-159">phoneAlias</span><span class="sxs-lookup"><span data-stu-id="2c584-159">phoneAlias</span></span>  

<!-- -->

<span data-ttu-id="2c584-160">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="2c584-160">phoneNumber</span></span>  

