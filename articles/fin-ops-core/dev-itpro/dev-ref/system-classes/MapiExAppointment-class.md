---
title: MapiExAppointment クラス
description: このトピックでは、MapiExAppointment クラスについて説明します。
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
ms.openlocfilehash: e075c00ce631a00624a6c69021b58c903e7843c6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502586"
---
# <a name="class-mapiexappointment"></a><span data-ttu-id="3b8dd-103">クラス MapiExAppointment</span><span class="sxs-lookup"><span data-stu-id="3b8dd-103">Class MapiExAppointment</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class MapiExAppointment extends MapiExMessage
```

## <a name="remarks"></a><span data-ttu-id="3b8dd-104">備考</span><span class="sxs-lookup"><span data-stu-id="3b8dd-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="3b8dd-105">例</span><span class="sxs-lookup"><span data-stu-id="3b8dd-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="3b8dd-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="3b8dd-106">Methods</span></span>

| <span data-ttu-id="3b8dd-107">方法</span><span class="sxs-lookup"><span data-stu-id="3b8dd-107">Method</span></span>                                                 | <span data-ttu-id="3b8dd-108">説明</span><span class="sxs-lookup"><span data-stu-id="3b8dd-108">Description</span></span>                                                |
|--------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3b8dd-109">public str addRecipient(str email, str name, int type)</span><span class="sxs-lookup"><span data-stu-id="3b8dd-109">public str addRecipient(str email, str name, int type)</span></span> |                                                            |
| <span data-ttu-id="3b8dd-110">public str entryId()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-110">public str entryId()</span></span>                                   |                                                            |
| <span data-ttu-id="3b8dd-111">public str getGlobalObjectId()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-111">public str getGlobalObjectId()</span></span>                         |                                                            |
| <span data-ttu-id="3b8dd-112">public boolean getRecipient(int index)</span><span class="sxs-lookup"><span data-stu-id="3b8dd-112">public boolean getRecipient(int index)</span></span>                 |                                                            |
| <span data-ttu-id="3b8dd-113">public int getRecipientCount()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-113">public int getRecipientCount()</span></span>                         |                                                            |
| <span data-ttu-id="3b8dd-114">public str getRecipientDisplayName()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-114">public str getRecipientDisplayName()</span></span>                   |                                                            |
| <span data-ttu-id="3b8dd-115">public str getRecipientEmailAddress()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-115">public str getRecipientEmailAddress()</span></span>                  |                                                            |
| <span data-ttu-id="3b8dd-116">public str getRecipientEntryId()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-116">public str getRecipientEntryId()</span></span>                       |                                                            |
| <span data-ttu-id="3b8dd-117">public boolean getRecipients()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-117">public boolean getRecipients()</span></span>                         |                                                            |
| <span data-ttu-id="3b8dd-118">public str getRecipientSMTPAddress()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-118">public str getRecipientSMTPAddress()</span></span>                   |                                                            |
| <span data-ttu-id="3b8dd-119">public int getRecipientType()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-119">public int getRecipientType()</span></span>                          |                                                            |
| <span data-ttu-id="3b8dd-120">public str getSenderEmail()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-120">public str getSenderEmail()</span></span>                            |                                                            |
| <span data-ttu-id="3b8dd-121">public str getSenderName()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-121">public str getSenderName()</span></span>                             |                                                            |
| <span data-ttu-id="3b8dd-122">public str removeRecipient(str email, int type)</span><span class="sxs-lookup"><span data-stu-id="3b8dd-122">public str removeRecipient(str email, int type)</span></span>        |                                                            |
| <span data-ttu-id="3b8dd-123">public boolean save()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-123">public boolean save()</span></span>                                  |                                                            |
| <span data-ttu-id="3b8dd-124">public boolean setBody(str body)</span><span class="sxs-lookup"><span data-stu-id="3b8dd-124">public boolean setBody(str body)</span></span>                       |                                                            |
| <span data-ttu-id="3b8dd-125">public void new()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-125">public void new()</span></span>                                      | <span data-ttu-id="3b8dd-126">MapiExAppointment クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3b8dd-126">Initializes a new instance of the MapiExAppointment class.</span></span> |
| <span data-ttu-id="3b8dd-127">public void close()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-127">public void close()</span></span>                                    |                                                            |
| <span data-ttu-id="3b8dd-128">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="3b8dd-128">public void finalize()</span></span>                                 |                                                            |

## <a name="method-addrecipient"></a><span data-ttu-id="3b8dd-129">メソッド addRecipient</span><span class="sxs-lookup"><span data-stu-id="3b8dd-129">Method addRecipient</span></span>

```xpp
public str addRecipient(str email, str name, int type)
```

### <a name="parameters---addrecipient"></a><span data-ttu-id="3b8dd-130">パラメーター - addRecipient</span><span class="sxs-lookup"><span data-stu-id="3b8dd-130">Parameters - addRecipient</span></span>

<span data-ttu-id="3b8dd-131">電子メール</span><span class="sxs-lookup"><span data-stu-id="3b8dd-131">email</span></span>  

<!-- -->

<span data-ttu-id="3b8dd-132">名前</span><span class="sxs-lookup"><span data-stu-id="3b8dd-132">name</span></span>  

<!-- -->

<span data-ttu-id="3b8dd-133">タイプ</span><span class="sxs-lookup"><span data-stu-id="3b8dd-133">type</span></span>  

### <a name="return-value---addrecipient"></a><span data-ttu-id="3b8dd-134">戻り値 - addRefCnt</span><span class="sxs-lookup"><span data-stu-id="3b8dd-134">Return Value - addRecipient</span></span>

## <a name="method-entryid"></a><span data-ttu-id="3b8dd-135">メソッド entryId</span><span class="sxs-lookup"><span data-stu-id="3b8dd-135">Method entryId</span></span>

```xpp
public str entryId()
```

### <a name="return-value---entryid"></a><span data-ttu-id="3b8dd-136">戻り値 - entryId</span><span class="sxs-lookup"><span data-stu-id="3b8dd-136">Return Value - entryId</span></span>

## <a name="method-getglobalobjectid"></a><span data-ttu-id="3b8dd-137">メソッド getGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="3b8dd-137">Method getGlobalObjectId</span></span>

```xpp
public str getGlobalObjectId()
```

### <a name="return-value---getglobalobjectid"></a><span data-ttu-id="3b8dd-138">戻り値 - getGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="3b8dd-138">Return Value - getGlobalObjectId</span></span>

## <a name="method-getrecipient"></a><span data-ttu-id="3b8dd-139">メソッド getRecipient</span><span class="sxs-lookup"><span data-stu-id="3b8dd-139">Method getRecipient</span></span>

```xpp
public boolean getRecipient(int index)
```

### <a name="parameters---getrecipient"></a><span data-ttu-id="3b8dd-140">戻り値 - getRecipient</span><span class="sxs-lookup"><span data-stu-id="3b8dd-140">Parameters - getRecipient</span></span>

<span data-ttu-id="3b8dd-141">指数</span><span class="sxs-lookup"><span data-stu-id="3b8dd-141">index</span></span>  

### <a name="return-value---getrecipient"></a><span data-ttu-id="3b8dd-142">戻り値 - getRecipient</span><span class="sxs-lookup"><span data-stu-id="3b8dd-142">Return Value - getRecipient</span></span>

## <a name="method-getrecipientcount"></a><span data-ttu-id="3b8dd-143">メソッド getRecipientCount</span><span class="sxs-lookup"><span data-stu-id="3b8dd-143">Method getRecipientCount</span></span>

```xpp
public int getRecipientCount()
```

### <a name="return-value---getrecipientcount"></a><span data-ttu-id="3b8dd-144">戻り値 - getRecipientCount</span><span class="sxs-lookup"><span data-stu-id="3b8dd-144">Return Value - getRecipientCount</span></span>

## <a name="method-getrecipientdisplayname"></a><span data-ttu-id="3b8dd-145">メソッド getRecipientDisplayName</span><span class="sxs-lookup"><span data-stu-id="3b8dd-145">Method getRecipientDisplayName</span></span>

```xpp
public str getRecipientDisplayName()
```

### <a name="return-value---getrecipientdisplayname"></a><span data-ttu-id="3b8dd-146">戻り値 - getRecipientDisplayName</span><span class="sxs-lookup"><span data-stu-id="3b8dd-146">Return Value - getRecipientDisplayName</span></span>

## <a name="method-getrecipientemailaddress"></a><span data-ttu-id="3b8dd-147">メソッド getRecipientEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3b8dd-147">Method getRecipientEmailAddress</span></span>

```xpp
public str getRecipientEmailAddress()
```

### <a name="return-value---getrecipientemailaddress"></a><span data-ttu-id="3b8dd-148">戻り値 - getRecipientEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3b8dd-148">Return Value - getRecipientEmailAddress</span></span>

## <a name="method-getrecipiententryid"></a><span data-ttu-id="3b8dd-149">メソッド getRecipientEntryId</span><span class="sxs-lookup"><span data-stu-id="3b8dd-149">Method getRecipientEntryId</span></span>

```xpp
public str getRecipientEntryId()
```

### <a name="return-value---getrecipiententryid"></a><span data-ttu-id="3b8dd-150">戻り値 - getRecipientCount</span><span class="sxs-lookup"><span data-stu-id="3b8dd-150">Return Value - getRecipientEntryId</span></span>

## <a name="method-getrecipients"></a><span data-ttu-id="3b8dd-151">メソッド getRecipients</span><span class="sxs-lookup"><span data-stu-id="3b8dd-151">Method getRecipients</span></span>

```xpp
public boolean getRecipients()
```

### <a name="return-value---getrecipients"></a><span data-ttu-id="3b8dd-152">戻り値 - getRecipients</span><span class="sxs-lookup"><span data-stu-id="3b8dd-152">Return Value - getRecipients</span></span>

## <a name="method-getrecipientsmtpaddress"></a><span data-ttu-id="3b8dd-153">メソッド getRecipientSMTPAddress</span><span class="sxs-lookup"><span data-stu-id="3b8dd-153">Method getRecipientSMTPAddress</span></span>

```xpp
public str getRecipientSMTPAddress()
```

### <a name="return-value---getrecipientsmtpaddress"></a><span data-ttu-id="3b8dd-154">戻り値 - getRecipientSMTPAddress</span><span class="sxs-lookup"><span data-stu-id="3b8dd-154">Return Value - getRecipientSMTPAddress</span></span>

## <a name="method-getrecipienttype"></a><span data-ttu-id="3b8dd-155">メソッド getRecipientType</span><span class="sxs-lookup"><span data-stu-id="3b8dd-155">Method getRecipientType</span></span>

```xpp
public int getRecipientType()
```

### <a name="return-value---getrecipienttype"></a><span data-ttu-id="3b8dd-156">戻り値 - getRecipientType</span><span class="sxs-lookup"><span data-stu-id="3b8dd-156">Return Value - getRecipientType</span></span>

## <a name="method-getsenderemail"></a><span data-ttu-id="3b8dd-157">メソッド getSenderEmail</span><span class="sxs-lookup"><span data-stu-id="3b8dd-157">Method getSenderEmail</span></span>

```xpp
public str getSenderEmail()
```

### <a name="return-value---getsenderemail"></a><span data-ttu-id="3b8dd-158">戻り値 - getSenderEmail</span><span class="sxs-lookup"><span data-stu-id="3b8dd-158">Return Value - getSenderEmail</span></span>

## <a name="method-getsendername"></a><span data-ttu-id="3b8dd-159">メソッド getSenderName</span><span class="sxs-lookup"><span data-stu-id="3b8dd-159">Method getSenderName</span></span>

```xpp
public str getSenderName()
```

### <a name="return-value---getsendername"></a><span data-ttu-id="3b8dd-160">戻り値 - getSenderName</span><span class="sxs-lookup"><span data-stu-id="3b8dd-160">Return Value - getSenderName</span></span>

## <a name="method-removerecipient"></a><span data-ttu-id="3b8dd-161">メソッド removeRecipient</span><span class="sxs-lookup"><span data-stu-id="3b8dd-161">Method removeRecipient</span></span>

```xpp
public str removeRecipient(str email, int type)
```

### <a name="parameters---removerecipient"></a><span data-ttu-id="3b8dd-162">パラメーター - removeRecipient</span><span class="sxs-lookup"><span data-stu-id="3b8dd-162">Parameters - removeRecipient</span></span>

<span data-ttu-id="3b8dd-163">電子メール</span><span class="sxs-lookup"><span data-stu-id="3b8dd-163">email</span></span>  

<!-- -->

<span data-ttu-id="3b8dd-164">タイプ</span><span class="sxs-lookup"><span data-stu-id="3b8dd-164">type</span></span>  

### <a name="return-value---removerecipient"></a><span data-ttu-id="3b8dd-165">戻り値 - removeRecipient</span><span class="sxs-lookup"><span data-stu-id="3b8dd-165">Return Value - removeRecipient</span></span>

## <a name="method-save"></a><span data-ttu-id="3b8dd-166">メソッド save</span><span class="sxs-lookup"><span data-stu-id="3b8dd-166">Method save</span></span>

```xpp
public boolean save()
```

### <a name="return-value---save"></a><span data-ttu-id="3b8dd-167">戻り値 - save</span><span class="sxs-lookup"><span data-stu-id="3b8dd-167">Return Value - save</span></span>

## <a name="method-setbody"></a><span data-ttu-id="3b8dd-168">メソッド setBody</span><span class="sxs-lookup"><span data-stu-id="3b8dd-168">Method setBody</span></span>

```xpp
public boolean setBody(str body)
```

### <a name="parameters---setbody"></a><span data-ttu-id="3b8dd-169">パラメーター - setBody</span><span class="sxs-lookup"><span data-stu-id="3b8dd-169">Parameters - setBody</span></span>

<span data-ttu-id="3b8dd-170">body</span><span class="sxs-lookup"><span data-stu-id="3b8dd-170">body</span></span>  

### <a name="return-value---setbody"></a><span data-ttu-id="3b8dd-171">戻り値 - setBody</span><span class="sxs-lookup"><span data-stu-id="3b8dd-171">Return Value - setBody</span></span>

## <a name="method-new"></a><span data-ttu-id="3b8dd-172">メソッド new</span><span class="sxs-lookup"><span data-stu-id="3b8dd-172">Method new</span></span>

<span data-ttu-id="3b8dd-173">MapiExAppointment クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3b8dd-173">Initializes a new instance of the MapiExAppointment class.</span></span>

```xpp
public void new()
```

## <a name="method-close"></a><span data-ttu-id="3b8dd-174">メソッド close</span><span class="sxs-lookup"><span data-stu-id="3b8dd-174">Method close</span></span>

```xpp
public void close()
```

## <a name="method-finalize"></a><span data-ttu-id="3b8dd-175">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="3b8dd-175">Method finalize</span></span>

```xpp
public void finalize()
```

