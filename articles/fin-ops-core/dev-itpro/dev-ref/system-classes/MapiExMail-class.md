---
title: MapiExMail クラス
description: このトピックでは、MapiExMail クラスについて説明します。
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
ms.openlocfilehash: 4a11e39b6a7f8a873c646dab8de1d1cdef955826
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502583"
---
# <a name="class-mapiexmail"></a><span data-ttu-id="962f1-103">クラス MapiExMail</span><span class="sxs-lookup"><span data-stu-id="962f1-103">Class MapiExMail</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class MapiExMail extends MapiExMessage
```

## <a name="remarks"></a><span data-ttu-id="962f1-104">備考</span><span class="sxs-lookup"><span data-stu-id="962f1-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="962f1-105">例</span><span class="sxs-lookup"><span data-stu-id="962f1-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="962f1-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="962f1-106">Methods</span></span>

| <span data-ttu-id="962f1-107">方法</span><span class="sxs-lookup"><span data-stu-id="962f1-107">Method</span></span>                                                 | <span data-ttu-id="962f1-108">説明</span><span class="sxs-lookup"><span data-stu-id="962f1-108">Description</span></span>                                         |
|--------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="962f1-109">public str addRecipient(str email, str name, int type)</span><span class="sxs-lookup"><span data-stu-id="962f1-109">public str addRecipient(str email, str name, int type)</span></span> |                                                     |
| <span data-ttu-id="962f1-110">public str entryId()</span><span class="sxs-lookup"><span data-stu-id="962f1-110">public str entryId()</span></span>                                   |                                                     |
| <span data-ttu-id="962f1-111">public boolean getRecipient(int index)</span><span class="sxs-lookup"><span data-stu-id="962f1-111">public boolean getRecipient(int index)</span></span>                 |                                                     |
| <span data-ttu-id="962f1-112">public int getRecipientCount()</span><span class="sxs-lookup"><span data-stu-id="962f1-112">public int getRecipientCount()</span></span>                         |                                                     |
| <span data-ttu-id="962f1-113">public str getRecipientDisplayName()</span><span class="sxs-lookup"><span data-stu-id="962f1-113">public str getRecipientDisplayName()</span></span>                   |                                                     |
| <span data-ttu-id="962f1-114">public str getRecipientEmailAddress()</span><span class="sxs-lookup"><span data-stu-id="962f1-114">public str getRecipientEmailAddress()</span></span>                  |                                                     |
| <span data-ttu-id="962f1-115">public str getRecipientEntryId()</span><span class="sxs-lookup"><span data-stu-id="962f1-115">public str getRecipientEntryId()</span></span>                       |                                                     |
| <span data-ttu-id="962f1-116">public boolean getRecipients()</span><span class="sxs-lookup"><span data-stu-id="962f1-116">public boolean getRecipients()</span></span>                         |                                                     |
| <span data-ttu-id="962f1-117">public str getRecipientSMTPAddress()</span><span class="sxs-lookup"><span data-stu-id="962f1-117">public str getRecipientSMTPAddress()</span></span>                   |                                                     |
| <span data-ttu-id="962f1-118">public int getRecipientType()</span><span class="sxs-lookup"><span data-stu-id="962f1-118">public int getRecipientType()</span></span>                          |                                                     |
| <span data-ttu-id="962f1-119">public str getSenderEmail()</span><span class="sxs-lookup"><span data-stu-id="962f1-119">public str getSenderEmail()</span></span>                            |                                                     |
| <span data-ttu-id="962f1-120">public str getSenderName()</span><span class="sxs-lookup"><span data-stu-id="962f1-120">public str getSenderName()</span></span>                             |                                                     |
| <span data-ttu-id="962f1-121">public str removeRecipient(str email, int type)</span><span class="sxs-lookup"><span data-stu-id="962f1-121">public str removeRecipient(str email, int type)</span></span>        |                                                     |
| <span data-ttu-id="962f1-122">public boolean save()</span><span class="sxs-lookup"><span data-stu-id="962f1-122">public boolean save()</span></span>                                  |                                                     |
| <span data-ttu-id="962f1-123">public boolean saveMsgToFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="962f1-123">public boolean saveMsgToFile(str fileName)</span></span>             |                                                     |
| <span data-ttu-id="962f1-124">public boolean send()</span><span class="sxs-lookup"><span data-stu-id="962f1-124">public boolean send()</span></span>                                  |                                                     |
| <span data-ttu-id="962f1-125">public boolean setBody(str body)</span><span class="sxs-lookup"><span data-stu-id="962f1-125">public boolean setBody(str body)</span></span>                       |                                                     |
| <span data-ttu-id="962f1-126">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="962f1-126">public void finalize()</span></span>                                 |                                                     |
| <span data-ttu-id="962f1-127">public void close()</span><span class="sxs-lookup"><span data-stu-id="962f1-127">public void close()</span></span>                                    |                                                     |
| <span data-ttu-id="962f1-128">public void new()</span><span class="sxs-lookup"><span data-stu-id="962f1-128">public void new()</span></span>                                      | <span data-ttu-id="962f1-129">MapiExMail クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="962f1-129">Initializes a new instance of the MapiExMail class.</span></span> |

## <a name="method-addrecipient"></a><span data-ttu-id="962f1-130">メソッド addRecipient</span><span class="sxs-lookup"><span data-stu-id="962f1-130">Method addRecipient</span></span>

```xpp
public str addRecipient(str email, str name, int type)
```

### <a name="parameters---addrecipient"></a><span data-ttu-id="962f1-131">パラメーター - addRecipient</span><span class="sxs-lookup"><span data-stu-id="962f1-131">Parameters - addRecipient</span></span>

<span data-ttu-id="962f1-132">電子メール</span><span class="sxs-lookup"><span data-stu-id="962f1-132">email</span></span>  

<!-- -->

<span data-ttu-id="962f1-133">名前</span><span class="sxs-lookup"><span data-stu-id="962f1-133">name</span></span>  

<!-- -->

<span data-ttu-id="962f1-134">タイプ</span><span class="sxs-lookup"><span data-stu-id="962f1-134">type</span></span>  

### <a name="return-value---addrecipient"></a><span data-ttu-id="962f1-135">戻り値 - addRefCnt</span><span class="sxs-lookup"><span data-stu-id="962f1-135">Return Value - addRecipient</span></span>

## <a name="method-entryid"></a><span data-ttu-id="962f1-136">メソッド entryId</span><span class="sxs-lookup"><span data-stu-id="962f1-136">Method entryId</span></span>

```xpp
public str entryId()
```

### <a name="return-value---entryid"></a><span data-ttu-id="962f1-137">戻り値 - entryId</span><span class="sxs-lookup"><span data-stu-id="962f1-137">Return Value - entryId</span></span>

## <a name="method-getrecipient"></a><span data-ttu-id="962f1-138">メソッド getRecipient</span><span class="sxs-lookup"><span data-stu-id="962f1-138">Method getRecipient</span></span>

```xpp
public boolean getRecipient(int index)
```

### <a name="parameters---getrecipient"></a><span data-ttu-id="962f1-139">戻り値 - getRecipient</span><span class="sxs-lookup"><span data-stu-id="962f1-139">Parameters - getRecipient</span></span>

<span data-ttu-id="962f1-140">指数</span><span class="sxs-lookup"><span data-stu-id="962f1-140">index</span></span>  

### <a name="return-value---getrecipient"></a><span data-ttu-id="962f1-141">戻り値 - getRecipient</span><span class="sxs-lookup"><span data-stu-id="962f1-141">Return Value - getRecipient</span></span>

## <a name="method-getrecipientcount"></a><span data-ttu-id="962f1-142">メソッド getRecipientCount</span><span class="sxs-lookup"><span data-stu-id="962f1-142">Method getRecipientCount</span></span>

```xpp
public int getRecipientCount()
```

### <a name="return-value---getrecipientcount"></a><span data-ttu-id="962f1-143">戻り値 - getRecipientCount</span><span class="sxs-lookup"><span data-stu-id="962f1-143">Return Value - getRecipientCount</span></span>

## <a name="method-getrecipientdisplayname"></a><span data-ttu-id="962f1-144">メソッド getRecipientDisplayName</span><span class="sxs-lookup"><span data-stu-id="962f1-144">Method getRecipientDisplayName</span></span>

```xpp
public str getRecipientDisplayName()
```

### <a name="return-value---getrecipientdisplayname"></a><span data-ttu-id="962f1-145">戻り値 - getRecipientDisplayName</span><span class="sxs-lookup"><span data-stu-id="962f1-145">Return Value - getRecipientDisplayName</span></span>

## <a name="method-getrecipientemailaddress"></a><span data-ttu-id="962f1-146">メソッド getRecipientEmailAddress</span><span class="sxs-lookup"><span data-stu-id="962f1-146">Method getRecipientEmailAddress</span></span>

```xpp
public str getRecipientEmailAddress()
```

### <a name="return-value---getrecipientemailaddress"></a><span data-ttu-id="962f1-147">戻り値 - getRecipientEmailAddress</span><span class="sxs-lookup"><span data-stu-id="962f1-147">Return Value - getRecipientEmailAddress</span></span>

## <a name="method-getrecipiententryid"></a><span data-ttu-id="962f1-148">メソッド getRecipientEntryId</span><span class="sxs-lookup"><span data-stu-id="962f1-148">Method getRecipientEntryId</span></span>

```xpp
public str getRecipientEntryId()
```

### <a name="return-value---getrecipiententryid"></a><span data-ttu-id="962f1-149">戻り値 - getRecipientCount</span><span class="sxs-lookup"><span data-stu-id="962f1-149">Return Value - getRecipientEntryId</span></span>

## <a name="method-getrecipients"></a><span data-ttu-id="962f1-150">メソッド getRecipients</span><span class="sxs-lookup"><span data-stu-id="962f1-150">Method getRecipients</span></span>

```xpp
public boolean getRecipients()
```

### <a name="return-value---getrecipients"></a><span data-ttu-id="962f1-151">戻り値 - getRecipients</span><span class="sxs-lookup"><span data-stu-id="962f1-151">Return Value - getRecipients</span></span>

## <a name="method-getrecipientsmtpaddress"></a><span data-ttu-id="962f1-152">メソッド getRecipientSMTPAddress</span><span class="sxs-lookup"><span data-stu-id="962f1-152">Method getRecipientSMTPAddress</span></span>

```xpp
public str getRecipientSMTPAddress()
```

### <a name="return-value---getrecipientsmtpaddress"></a><span data-ttu-id="962f1-153">戻り値 - getRecipientSMTPAddress</span><span class="sxs-lookup"><span data-stu-id="962f1-153">Return Value - getRecipientSMTPAddress</span></span>

## <a name="method-getrecipienttype"></a><span data-ttu-id="962f1-154">メソッド getRecipientType</span><span class="sxs-lookup"><span data-stu-id="962f1-154">Method getRecipientType</span></span>

```xpp
public int getRecipientType()
```

### <a name="return-value---getrecipienttype"></a><span data-ttu-id="962f1-155">戻り値 - getRecipientType</span><span class="sxs-lookup"><span data-stu-id="962f1-155">Return Value - getRecipientType</span></span>

## <a name="method-getsenderemail"></a><span data-ttu-id="962f1-156">メソッド getSenderEmail</span><span class="sxs-lookup"><span data-stu-id="962f1-156">Method getSenderEmail</span></span>

```xpp
public str getSenderEmail()
```

### <a name="return-value---getsenderemail"></a><span data-ttu-id="962f1-157">戻り値 - getSenderEmail</span><span class="sxs-lookup"><span data-stu-id="962f1-157">Return Value - getSenderEmail</span></span>

## <a name="method-getsendername"></a><span data-ttu-id="962f1-158">メソッド getSenderName</span><span class="sxs-lookup"><span data-stu-id="962f1-158">Method getSenderName</span></span>

```xpp
public str getSenderName()
```

### <a name="return-value---getsendername"></a><span data-ttu-id="962f1-159">戻り値 - getSenderName</span><span class="sxs-lookup"><span data-stu-id="962f1-159">Return Value - getSenderName</span></span>

## <a name="method-removerecipient"></a><span data-ttu-id="962f1-160">メソッド removeRecipient</span><span class="sxs-lookup"><span data-stu-id="962f1-160">Method removeRecipient</span></span>

```xpp
public str removeRecipient(str email, int type)
```

### <a name="parameters---removerecipient"></a><span data-ttu-id="962f1-161">パラメーター - removeRecipient</span><span class="sxs-lookup"><span data-stu-id="962f1-161">Parameters - removeRecipient</span></span>

<span data-ttu-id="962f1-162">電子メール</span><span class="sxs-lookup"><span data-stu-id="962f1-162">email</span></span>  

<!-- -->

<span data-ttu-id="962f1-163">タイプ</span><span class="sxs-lookup"><span data-stu-id="962f1-163">type</span></span>  

### <a name="return-value---removerecipient"></a><span data-ttu-id="962f1-164">戻り値 - removeRecipient</span><span class="sxs-lookup"><span data-stu-id="962f1-164">Return Value - removeRecipient</span></span>

## <a name="method-save"></a><span data-ttu-id="962f1-165">メソッド save</span><span class="sxs-lookup"><span data-stu-id="962f1-165">Method save</span></span>

```xpp
public boolean save()
```

### <a name="return-value---save"></a><span data-ttu-id="962f1-166">戻り値 - save</span><span class="sxs-lookup"><span data-stu-id="962f1-166">Return Value - save</span></span>

## <a name="method-savemsgtofile"></a><span data-ttu-id="962f1-167">メソッド saveMsgToFile</span><span class="sxs-lookup"><span data-stu-id="962f1-167">Method saveMsgToFile</span></span>

```xpp
public boolean saveMsgToFile(str fileName)
```

### <a name="parameters---savemsgtofile"></a><span data-ttu-id="962f1-168">パラメーター - saveMsgToFile</span><span class="sxs-lookup"><span data-stu-id="962f1-168">Parameters - saveMsgToFile</span></span>

<span data-ttu-id="962f1-169">fileName</span><span class="sxs-lookup"><span data-stu-id="962f1-169">fileName</span></span>  

### <a name="return-value---savemsgtofile"></a><span data-ttu-id="962f1-170">戻り値 - saveMsgToFile</span><span class="sxs-lookup"><span data-stu-id="962f1-170">Return Value - saveMsgToFile</span></span>

## <a name="method-send"></a><span data-ttu-id="962f1-171">メソッド send</span><span class="sxs-lookup"><span data-stu-id="962f1-171">Method send</span></span>

```xpp
public boolean send()
```

### <a name="return-value---send"></a><span data-ttu-id="962f1-172">戻り値 - send</span><span class="sxs-lookup"><span data-stu-id="962f1-172">Return Value - send</span></span>

## <a name="method-setbody"></a><span data-ttu-id="962f1-173">メソッド setBody</span><span class="sxs-lookup"><span data-stu-id="962f1-173">Method setBody</span></span>

```xpp
public boolean setBody(str body)
```

### <a name="parameters---setbody"></a><span data-ttu-id="962f1-174">パラメーター - setBody</span><span class="sxs-lookup"><span data-stu-id="962f1-174">Parameters - setBody</span></span>

<span data-ttu-id="962f1-175">body</span><span class="sxs-lookup"><span data-stu-id="962f1-175">body</span></span>  

### <a name="return-value---setbody"></a><span data-ttu-id="962f1-176">戻り値 - setBody</span><span class="sxs-lookup"><span data-stu-id="962f1-176">Return Value - setBody</span></span>

## <a name="method-finalize"></a><span data-ttu-id="962f1-177">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="962f1-177">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-close"></a><span data-ttu-id="962f1-178">メソッド close</span><span class="sxs-lookup"><span data-stu-id="962f1-178">Method close</span></span>

```xpp
public void close()
```

## <a name="method-new"></a><span data-ttu-id="962f1-179">メソッド new</span><span class="sxs-lookup"><span data-stu-id="962f1-179">Method new</span></span>

<span data-ttu-id="962f1-180">MapiExMail クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="962f1-180">Initializes a new instance of the MapiExMail class.</span></span>

```xpp
public void new()
```

