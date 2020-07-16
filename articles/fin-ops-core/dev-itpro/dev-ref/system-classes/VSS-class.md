---
title: VSS クラス
description: このトピックでは、VSS クラスについて説明します。
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
ms.openlocfilehash: a174fc7f84401839952f697e9fb30218cf5086f4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502778"
---
# <a name="class-vss"></a><span data-ttu-id="ae52a-103">クラス VSS</span><span class="sxs-lookup"><span data-stu-id="ae52a-103">Class VSS</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class VSS extends Object
```

## <a name="remarks"></a><span data-ttu-id="ae52a-104">備考</span><span class="sxs-lookup"><span data-stu-id="ae52a-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="ae52a-105">例</span><span class="sxs-lookup"><span data-stu-id="ae52a-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="ae52a-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="ae52a-106">Methods</span></span>

| <span data-ttu-id="ae52a-107">方法</span><span class="sxs-lookup"><span data-stu-id="ae52a-107">Method</span></span>                                                                                                        | <span data-ttu-id="ae52a-108">説明</span><span class="sxs-lookup"><span data-stu-id="ae52a-108">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="ae52a-109">public boolean connect()</span><span class="sxs-lookup"><span data-stu-id="ae52a-109">public boolean connect()</span></span>                                                                                      |                                           |
| <span data-ttu-id="ae52a-110">public boolean connected()</span><span class="sxs-lookup"><span data-stu-id="ae52a-110">public boolean connected()</span></span>                                                                                    |                                           |
| <span data-ttu-id="ae52a-111">public boolean disconnect()</span><span class="sxs-lookup"><span data-stu-id="ae52a-111">public boolean disconnect()</span></span>                                                                                   |                                           |
| <span data-ttu-id="ae52a-112">public container getCheckedoutFiles()</span><span class="sxs-lookup"><span data-stu-id="ae52a-112">public container getCheckedoutFiles()</span></span>                                                                         |                                           |
| <span data-ttu-id="ae52a-113">public container getConnectionInfo()</span><span class="sxs-lookup"><span data-stu-id="ae52a-113">public container getConnectionInfo()</span></span>                                                                          |                                           |
| <span data-ttu-id="ae52a-114">public VSSItem getVSSItem(str vssItemPath, str localFilePath, \[boolean completePath\], \[int version\])</span><span class="sxs-lookup"><span data-stu-id="ae52a-114">public VSSItem getVSSItem(str vssItemPath, str localFilePath, \[boolean completePath\], \[int version\])</span></span>      |                                           |
| <span data-ttu-id="ae52a-115">public boolean init(str vssIni, str vssPrjRoot, str vssWorkingFolder, str vssUser, str vssPwd)</span><span class="sxs-lookup"><span data-stu-id="ae52a-115">public boolean init(str vssIni, str vssPrjRoot, str vssWorkingFolder, str vssUser, str vssPwd)</span></span>                |                                           |
| <span data-ttu-id="ae52a-116">public VSSItem newSubProject(str name, str localPath)</span><span class="sxs-lookup"><span data-stu-id="ae52a-116">public VSSItem newSubProject(str name, str localPath)</span></span>                                                         |                                           |
| <span data-ttu-id="ae52a-117">public Map synchronizeProjects(\[Set projects\], \[boolean force\], \[boolean delLocalFiles\], \[str label\])</span><span class="sxs-lookup"><span data-stu-id="ae52a-117">public Map synchronizeProjects(\[Set projects\], \[boolean force\], \[boolean delLocalFiles\], \[str label\])</span></span> |                                           |
| <span data-ttu-id="ae52a-118">public void new()</span><span class="sxs-lookup"><span data-stu-id="ae52a-118">public void new()</span></span>                                                                                             | <span data-ttu-id="ae52a-119">VSS クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ae52a-119">Initializes an instance of the VSS class.</span></span> |

## <a name="method-connect"></a><span data-ttu-id="ae52a-120">メソッド connect</span><span class="sxs-lookup"><span data-stu-id="ae52a-120">Method connect</span></span>

```xpp
public boolean connect()
```

### <a name="return-value---connect"></a><span data-ttu-id="ae52a-121">戻り値 - connect</span><span class="sxs-lookup"><span data-stu-id="ae52a-121">Return Value - connect</span></span>

## <a name="method-connected"></a><span data-ttu-id="ae52a-122">メソッド connected</span><span class="sxs-lookup"><span data-stu-id="ae52a-122">Method connected</span></span>

```xpp
public boolean connected()
```

### <a name="return-value---connected"></a><span data-ttu-id="ae52a-123">戻り値 - connected</span><span class="sxs-lookup"><span data-stu-id="ae52a-123">Return Value - connected</span></span>

## <a name="method-disconnect"></a><span data-ttu-id="ae52a-124">メソッド disconnect</span><span class="sxs-lookup"><span data-stu-id="ae52a-124">Method disconnect</span></span>

```xpp
public boolean disconnect()
```

### <a name="return-value---disconnect"></a><span data-ttu-id="ae52a-125">戻り値 - disconnect</span><span class="sxs-lookup"><span data-stu-id="ae52a-125">Return Value - disconnect</span></span>

## <a name="method-getcheckedoutfiles"></a><span data-ttu-id="ae52a-126">メソッド getCheckedoutFiles</span><span class="sxs-lookup"><span data-stu-id="ae52a-126">Method getCheckedoutFiles</span></span>

```xpp
public container getCheckedoutFiles()
```

### <a name="return-value---getcheckedoutfiles"></a><span data-ttu-id="ae52a-127">戻り値 - getCheckedoutFiles</span><span class="sxs-lookup"><span data-stu-id="ae52a-127">Return Value - getCheckedoutFiles</span></span>

## <a name="method-getconnectioninfo"></a><span data-ttu-id="ae52a-128">メソッド getConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="ae52a-128">Method getConnectionInfo</span></span>

```xpp
public container getConnectionInfo()
```

### <a name="return-value---getconnectioninfo"></a><span data-ttu-id="ae52a-129">戻り値 - getConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="ae52a-129">Return Value - getConnectionInfo</span></span>

## <a name="method-getvssitem"></a><span data-ttu-id="ae52a-130">メソッド getVSSItem</span><span class="sxs-lookup"><span data-stu-id="ae52a-130">Method getVSSItem</span></span>

```xpp
public VSSItem getVSSItem(str vssItemPath, str localFilePath, [boolean completePath], [int version])
```

### <a name="parameters---getvssitem"></a><span data-ttu-id="ae52a-131">パラメーター - getVSSItem</span><span class="sxs-lookup"><span data-stu-id="ae52a-131">Parameters - getVSSItem</span></span>

<span data-ttu-id="ae52a-132">vssItemPath</span><span class="sxs-lookup"><span data-stu-id="ae52a-132">vssItemPath</span></span>  

<!-- -->

<span data-ttu-id="ae52a-133">localFilePath</span><span class="sxs-lookup"><span data-stu-id="ae52a-133">localFilePath</span></span>  

<!-- -->

<span data-ttu-id="ae52a-134">completePath</span><span class="sxs-lookup"><span data-stu-id="ae52a-134">completePath</span></span>  

<!-- -->

<span data-ttu-id="ae52a-135">のバージョン</span><span class="sxs-lookup"><span data-stu-id="ae52a-135">version</span></span>  

### <a name="return-value---getvssitem"></a><span data-ttu-id="ae52a-136">戻り値 - getVSSItem</span><span class="sxs-lookup"><span data-stu-id="ae52a-136">Return Value - getVSSItem</span></span>

## <a name="method-init"></a><span data-ttu-id="ae52a-137">メソッド init</span><span class="sxs-lookup"><span data-stu-id="ae52a-137">Method init</span></span>

```xpp
public boolean init(str vssIni, str vssPrjRoot, str vssWorkingFolder, str vssUser, str vssPwd)
```

### <a name="parameters---init"></a><span data-ttu-id="ae52a-138">パラメーター - init</span><span class="sxs-lookup"><span data-stu-id="ae52a-138">Parameters - init</span></span>

<span data-ttu-id="ae52a-139">vssIni</span><span class="sxs-lookup"><span data-stu-id="ae52a-139">vssIni</span></span>  

<!-- -->

<span data-ttu-id="ae52a-140">vssPrjRoot</span><span class="sxs-lookup"><span data-stu-id="ae52a-140">vssPrjRoot</span></span>  

<!-- -->

<span data-ttu-id="ae52a-141">vssWorkingFolder</span><span class="sxs-lookup"><span data-stu-id="ae52a-141">vssWorkingFolder</span></span>  

<!-- -->

<span data-ttu-id="ae52a-142">vssUser</span><span class="sxs-lookup"><span data-stu-id="ae52a-142">vssUser</span></span>  

<!-- -->

<span data-ttu-id="ae52a-143">vssPwd</span><span class="sxs-lookup"><span data-stu-id="ae52a-143">vssPwd</span></span>  

### <a name="return-value---init"></a><span data-ttu-id="ae52a-144">戻り値 - init</span><span class="sxs-lookup"><span data-stu-id="ae52a-144">Return Value - init</span></span>

## <a name="method-newsubproject"></a><span data-ttu-id="ae52a-145">メソッド newSubProject</span><span class="sxs-lookup"><span data-stu-id="ae52a-145">Method newSubProject</span></span>

```xpp
public VSSItem newSubProject(str name, str localPath)
```

### <a name="parameters---newsubproject"></a><span data-ttu-id="ae52a-146">パラメーター - newSubProject</span><span class="sxs-lookup"><span data-stu-id="ae52a-146">Parameters - newSubProject</span></span>

<span data-ttu-id="ae52a-147">名前</span><span class="sxs-lookup"><span data-stu-id="ae52a-147">name</span></span>  

<!-- -->

<span data-ttu-id="ae52a-148">localPath</span><span class="sxs-lookup"><span data-stu-id="ae52a-148">localPath</span></span>  

### <a name="return-value---newsubproject"></a><span data-ttu-id="ae52a-149">戻り値 - newSubProject</span><span class="sxs-lookup"><span data-stu-id="ae52a-149">Return Value - newSubProject</span></span>

## <a name="method-synchronizeprojects"></a><span data-ttu-id="ae52a-150">メソッド synchronizeProjects</span><span class="sxs-lookup"><span data-stu-id="ae52a-150">Method synchronizeProjects</span></span>

```xpp
public Map synchronizeProjects([Set projects], [boolean force], [boolean delLocalFiles], [str label])
```

### <a name="parameters---synchronizeprojects"></a><span data-ttu-id="ae52a-151">パラメーター - synchronizeProjects</span><span class="sxs-lookup"><span data-stu-id="ae52a-151">Parameters - synchronizeProjects</span></span>

<span data-ttu-id="ae52a-152">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="ae52a-152">projects</span></span>  

<!-- -->

<span data-ttu-id="ae52a-153">force</span><span class="sxs-lookup"><span data-stu-id="ae52a-153">force</span></span>  

<!-- -->

<span data-ttu-id="ae52a-154">delLocalFiles</span><span class="sxs-lookup"><span data-stu-id="ae52a-154">delLocalFiles</span></span>  

<!-- -->

<span data-ttu-id="ae52a-155">ラベル</span><span class="sxs-lookup"><span data-stu-id="ae52a-155">label</span></span>  

### <a name="return-value---synchronizeprojects"></a><span data-ttu-id="ae52a-156">戻り値 - synchronizeProjects</span><span class="sxs-lookup"><span data-stu-id="ae52a-156">Return Value - synchronizeProjects</span></span>

## <a name="method-new"></a><span data-ttu-id="ae52a-157">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ae52a-157">Method new</span></span>

<span data-ttu-id="ae52a-158">VSS クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ae52a-158">Initializes an instance of the VSS class.</span></span>

```xpp
public void new()
```

