---
title: MapiEx クラス
description: このトピックでは、MapiEx クラスについて説明します。
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
ms.openlocfilehash: ce6d856e09654c75fc4b9ef13640c068b8295892
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502587"
---
# <a name="class-mapiex"></a><span data-ttu-id="08a43-103">クラス MapiEx</span><span class="sxs-lookup"><span data-stu-id="08a43-103">Class MapiEx</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class MapiEx extends Object
```

## <a name="remarks"></a><span data-ttu-id="08a43-104">備考</span><span class="sxs-lookup"><span data-stu-id="08a43-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="08a43-105">例</span><span class="sxs-lookup"><span data-stu-id="08a43-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="08a43-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="08a43-106">Methods</span></span>

| <span data-ttu-id="08a43-107">方法</span><span class="sxs-lookup"><span data-stu-id="08a43-107">Method</span></span>                                                          | <span data-ttu-id="08a43-108">説明</span><span class="sxs-lookup"><span data-stu-id="08a43-108">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="08a43-109">public MapiExAppointment getAppointmentFromEntryId(str entryID)</span><span class="sxs-lookup"><span data-stu-id="08a43-109">public MapiExAppointment getAppointmentFromEntryId(str entryID)</span></span> |                                                 |
| <span data-ttu-id="08a43-110">public MapiExContact getContactFromEntryId(str entryID)</span><span class="sxs-lookup"><span data-stu-id="08a43-110">public MapiExContact getContactFromEntryId(str entryID)</span></span>         |                                                 |
| <span data-ttu-id="08a43-111">public int getCurrentUser()</span><span class="sxs-lookup"><span data-stu-id="08a43-111">public int getCurrentUser()</span></span>                                     |                                                 |
| <span data-ttu-id="08a43-112">public str getCurrentUserEmail()</span><span class="sxs-lookup"><span data-stu-id="08a43-112">public str getCurrentUserEmail()</span></span>                                |                                                 |
| <span data-ttu-id="08a43-113">public str getCurrentUserEntryId()</span><span class="sxs-lookup"><span data-stu-id="08a43-113">public str getCurrentUserEntryId()</span></span>                              |                                                 |
| <span data-ttu-id="08a43-114">public str getCurrentUserName()</span><span class="sxs-lookup"><span data-stu-id="08a43-114">public str getCurrentUserName()</span></span>                                 |                                                 |
| <span data-ttu-id="08a43-115">public MapiExMail getMailFromEntryId(str entryID)</span><span class="sxs-lookup"><span data-stu-id="08a43-115">public MapiExMail getMailFromEntryId(str entryID)</span></span>               |                                                 |
| <span data-ttu-id="08a43-116">public MapiExTask getTaskFromEntryId(str entryID)</span><span class="sxs-lookup"><span data-stu-id="08a43-116">public MapiExTask getTaskFromEntryId(str entryID)</span></span>               |                                                 |
| <span data-ttu-id="08a43-117">public int logon(str profileName, str password, int flags)</span><span class="sxs-lookup"><span data-stu-id="08a43-117">public int logon(str profileName, str password, int flags)</span></span>      |                                                 |
| <span data-ttu-id="08a43-118">public boolean mapiInitialised()</span><span class="sxs-lookup"><span data-stu-id="08a43-118">public boolean mapiInitialised()</span></span>                                |                                                 |
| <span data-ttu-id="08a43-119">public boolean openMessageStore(str str)</span><span class="sxs-lookup"><span data-stu-id="08a43-119">public boolean openMessageStore(str str)</span></span>                        |                                                 |
| <span data-ttu-id="08a43-120">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="08a43-120">public void finalize()</span></span>                                          |                                                 |
| <span data-ttu-id="08a43-121">public void new()</span><span class="sxs-lookup"><span data-stu-id="08a43-121">public void new()</span></span>                                               | <span data-ttu-id="08a43-122">MapiEx クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="08a43-122">Initializes a new instance of the MapiEx class.</span></span> |
| <span data-ttu-id="08a43-123">public void logout()</span><span class="sxs-lookup"><span data-stu-id="08a43-123">public void logout()</span></span>                                            |                                                 |

## <a name="method-getappointmentfromentryid"></a><span data-ttu-id="08a43-124">メソッド getAppointmentFromEntryId</span><span class="sxs-lookup"><span data-stu-id="08a43-124">Method getAppointmentFromEntryId</span></span>

```xpp
public MapiExAppointment getAppointmentFromEntryId(str entryID)
```

### <a name="parameters---getappointmentfromentryid"></a><span data-ttu-id="08a43-125">パラメーター - getAppointmentFromEntryId</span><span class="sxs-lookup"><span data-stu-id="08a43-125">Parameters - getAppointmentFromEntryId</span></span>

<span data-ttu-id="08a43-126">entryID</span><span class="sxs-lookup"><span data-stu-id="08a43-126">entryID</span></span>  

### <a name="return-value---getappointmentfromentryid"></a><span data-ttu-id="08a43-127">戻り値 - getAppointmentFromEntryId</span><span class="sxs-lookup"><span data-stu-id="08a43-127">Return Value - getAppointmentFromEntryId</span></span>

## <a name="method-getcontactfromentryid"></a><span data-ttu-id="08a43-128">メソッド getContactFromEntryId</span><span class="sxs-lookup"><span data-stu-id="08a43-128">Method getContactFromEntryId</span></span>

```xpp
public MapiExContact getContactFromEntryId(str entryID)
```

### <a name="parameters---getcontactfromentryid"></a><span data-ttu-id="08a43-129">パラメーター - getContactFromEntryId</span><span class="sxs-lookup"><span data-stu-id="08a43-129">Parameters - getContactFromEntryId</span></span>

<span data-ttu-id="08a43-130">entryID</span><span class="sxs-lookup"><span data-stu-id="08a43-130">entryID</span></span>  

### <a name="return-value---getcontactfromentryid"></a><span data-ttu-id="08a43-131">戻り値 - getContactFromEntryId</span><span class="sxs-lookup"><span data-stu-id="08a43-131">Return Value - getContactFromEntryId</span></span>

## <a name="method-getcurrentuser"></a><span data-ttu-id="08a43-132">メソッド getCurrentUser</span><span class="sxs-lookup"><span data-stu-id="08a43-132">Method getCurrentUser</span></span>

```xpp
public int getCurrentUser()
```

### <a name="return-value---getcurrentuser"></a><span data-ttu-id="08a43-133">戻り値 - getCurrentUser</span><span class="sxs-lookup"><span data-stu-id="08a43-133">Return Value - getCurrentUser</span></span>

## <a name="method-getcurrentuseremail"></a><span data-ttu-id="08a43-134">メソッド getCurrentUserEmail</span><span class="sxs-lookup"><span data-stu-id="08a43-134">Method getCurrentUserEmail</span></span>

```xpp
public str getCurrentUserEmail()
```

### <a name="return-value---getcurrentuseremail"></a><span data-ttu-id="08a43-135">戻り値 - getCurrentUserEmail</span><span class="sxs-lookup"><span data-stu-id="08a43-135">Return Value - getCurrentUserEmail</span></span>

## <a name="method-getcurrentuserentryid"></a><span data-ttu-id="08a43-136">メソッド getCurrentUserEntryId</span><span class="sxs-lookup"><span data-stu-id="08a43-136">Method getCurrentUserEntryId</span></span>

```xpp
public str getCurrentUserEntryId()
```

### <a name="return-value---getcurrentuserentryid"></a><span data-ttu-id="08a43-137">戻り値 - getCurrentUserEntryId</span><span class="sxs-lookup"><span data-stu-id="08a43-137">Return Value - getCurrentUserEntryId</span></span>

## <a name="method-getcurrentusername"></a><span data-ttu-id="08a43-138">メソッド getCurrentUserName</span><span class="sxs-lookup"><span data-stu-id="08a43-138">Method getCurrentUserName</span></span>

```xpp
public str getCurrentUserName()
```

### <a name="return-value---getcurrentusername"></a><span data-ttu-id="08a43-139">戻り値 - getCurrentUserName</span><span class="sxs-lookup"><span data-stu-id="08a43-139">Return Value - getCurrentUserName</span></span>

## <a name="method-getmailfromentryid"></a><span data-ttu-id="08a43-140">メソッド getMailFromEntryId</span><span class="sxs-lookup"><span data-stu-id="08a43-140">Method getMailFromEntryId</span></span>

```xpp
public MapiExMail getMailFromEntryId(str entryID)
```

### <a name="parameters---getmailfromentryid"></a><span data-ttu-id="08a43-141">パラメーター - getMailFromEntryId</span><span class="sxs-lookup"><span data-stu-id="08a43-141">Parameters - getMailFromEntryId</span></span>

<span data-ttu-id="08a43-142">entryID</span><span class="sxs-lookup"><span data-stu-id="08a43-142">entryID</span></span>  

### <a name="return-value---getmailfromentryid"></a><span data-ttu-id="08a43-143">戻り値 - getMailFromEntryId</span><span class="sxs-lookup"><span data-stu-id="08a43-143">Return Value - getMailFromEntryId</span></span>

## <a name="method-gettaskfromentryid"></a><span data-ttu-id="08a43-144">メソッド getTaskFromEntryId</span><span class="sxs-lookup"><span data-stu-id="08a43-144">Method getTaskFromEntryId</span></span>

```xpp
public MapiExTask getTaskFromEntryId(str entryID)
```

### <a name="parameters---gettaskfromentryid"></a><span data-ttu-id="08a43-145">パラメーター - getTaskFromEntryId</span><span class="sxs-lookup"><span data-stu-id="08a43-145">Parameters - getTaskFromEntryId</span></span>

<span data-ttu-id="08a43-146">entryID</span><span class="sxs-lookup"><span data-stu-id="08a43-146">entryID</span></span>  

### <a name="return-value---gettaskfromentryid"></a><span data-ttu-id="08a43-147">戻り値 - getTaskFromEntryId</span><span class="sxs-lookup"><span data-stu-id="08a43-147">Return Value - getTaskFromEntryId</span></span>

## <a name="method-logon"></a><span data-ttu-id="08a43-148">メソッド logon</span><span class="sxs-lookup"><span data-stu-id="08a43-148">Method logon</span></span>

```xpp
public int logon(str profileName, str password, int flags)
```

### <a name="parameters---logon"></a><span data-ttu-id="08a43-149">パラメーター - logon</span><span class="sxs-lookup"><span data-stu-id="08a43-149">Parameters - logon</span></span>

<span data-ttu-id="08a43-150">profileName</span><span class="sxs-lookup"><span data-stu-id="08a43-150">profileName</span></span>  

<!-- -->

<span data-ttu-id="08a43-151">パスワード</span><span class="sxs-lookup"><span data-stu-id="08a43-151">password</span></span>  

<!-- -->

<span data-ttu-id="08a43-152">flags</span><span class="sxs-lookup"><span data-stu-id="08a43-152">flags</span></span>  

### <a name="return-value---logon"></a><span data-ttu-id="08a43-153">戻り値 - logon</span><span class="sxs-lookup"><span data-stu-id="08a43-153">Return Value - logon</span></span>

## <a name="method-mapiinitialised"></a><span data-ttu-id="08a43-154">メソッド mapiInitialised</span><span class="sxs-lookup"><span data-stu-id="08a43-154">Method mapiInitialised</span></span>

```xpp
public boolean mapiInitialised()
```

### <a name="return-value---mapiinitialised"></a><span data-ttu-id="08a43-155">戻り値 - mapiInitialised</span><span class="sxs-lookup"><span data-stu-id="08a43-155">Return Value - mapiInitialised</span></span>

## <a name="method-openmessagestore"></a><span data-ttu-id="08a43-156">メソッド openMessageStore</span><span class="sxs-lookup"><span data-stu-id="08a43-156">Method openMessageStore</span></span>

```xpp
public boolean openMessageStore(str str)
```

### <a name="parameters---openmessagestore"></a><span data-ttu-id="08a43-157">パラメーター - openMessageStore</span><span class="sxs-lookup"><span data-stu-id="08a43-157">Parameters - openMessageStore</span></span>

<span data-ttu-id="08a43-158">str</span><span class="sxs-lookup"><span data-stu-id="08a43-158">str</span></span>  

### <a name="return-value---openmessagestore"></a><span data-ttu-id="08a43-159">戻り値 - openMessageStore</span><span class="sxs-lookup"><span data-stu-id="08a43-159">Return Value - openMessageStore</span></span>

## <a name="method-finalize"></a><span data-ttu-id="08a43-160">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="08a43-160">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="08a43-161">メソッド new</span><span class="sxs-lookup"><span data-stu-id="08a43-161">Method new</span></span>

<span data-ttu-id="08a43-162">MapiEx クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="08a43-162">Initializes a new instance of the MapiEx class.</span></span>

```xpp
public void new()
```

## <a name="method-logout"></a><span data-ttu-id="08a43-163">メソッド logout</span><span class="sxs-lookup"><span data-stu-id="08a43-163">Method logout</span></span>

```xpp
public void logout()
```

