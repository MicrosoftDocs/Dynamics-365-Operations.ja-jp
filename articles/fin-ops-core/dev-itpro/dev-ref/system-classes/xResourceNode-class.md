---
title: xResourceNode クラス
description: このトピックでは、xResourceNode クラスについて説明します。
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
ms.openlocfilehash: d1faadc69bdfe0b635b48751e43425450b8e227f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502759"
---
# <a name="class-xresourcenode"></a><span data-ttu-id="50551-103">クラス xResourceNode</span><span class="sxs-lookup"><span data-stu-id="50551-103">Class xResourceNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xResourceNode extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="50551-104">備考</span><span class="sxs-lookup"><span data-stu-id="50551-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="50551-105">例</span><span class="sxs-lookup"><span data-stu-id="50551-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="50551-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="50551-106">Methods</span></span>

| <span data-ttu-id="50551-107">方法</span><span class="sxs-lookup"><span data-stu-id="50551-107">Method</span></span>                                                                   | <span data-ttu-id="50551-108">説明</span><span class="sxs-lookup"><span data-stu-id="50551-108">Description</span></span> |
|--------------------------------------------------------------------------|-------------|
| <span data-ttu-id="50551-109">public BinData AOTGetData()</span><span class="sxs-lookup"><span data-stu-id="50551-109">public BinData AOTGetData()</span></span>                                              |             |
| <span data-ttu-id="50551-110">public Image AOTGetImage()</span><span class="sxs-lookup"><span data-stu-id="50551-110">public Image AOTGetImage()</span></span>                                               |             |
| <span data-ttu-id="50551-111">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50551-111">public str changedBy(\[str value\])</span></span>                                      |             |
| <span data-ttu-id="50551-112">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="50551-112">public Date changedDate(\[Date value\])</span></span>                                  |             |
| <span data-ttu-id="50551-113">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50551-113">public str changedTime(\[str value\])</span></span>                                    |             |
| <span data-ttu-id="50551-114">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="50551-114">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> |             |
| <span data-ttu-id="50551-115">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50551-115">public str createdBy(\[str value\])</span></span>                                      |             |
| <span data-ttu-id="50551-116">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="50551-116">public Date creationDate(\[Date value\])</span></span>                                 |             |
| <span data-ttu-id="50551-117">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50551-117">public str creationTime(\[str value\])</span></span>                                   |             |
| <span data-ttu-id="50551-118">public str filename(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50551-118">public str filename(\[str value\])</span></span>                                       |             |
| <span data-ttu-id="50551-119">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50551-119">public str helpText(\[str value\])</span></span>                                       |             |
| <span data-ttu-id="50551-120">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50551-120">public str label(\[str value\])</span></span>                                          |             |
| <span data-ttu-id="50551-121">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50551-121">public str name(\[str value\])</span></span>                                           |             |
| <span data-ttu-id="50551-122">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="50551-122">public Guid origin(\[Guid value\])</span></span>                                       |             |
| <span data-ttu-id="50551-123">::public static Image AOTCreateImage(str imageName)</span><span class="sxs-lookup"><span data-stu-id="50551-123">::public static Image AOTCreateImage(str imageName)</span></span>                      |             |
| <span data-ttu-id="50551-124">public void AOTSetData(BinData data)</span><span class="sxs-lookup"><span data-stu-id="50551-124">public void AOTSetData(BinData data)</span></span>                                     |             |
| <span data-ttu-id="50551-125">public void AOTSetImage(Image image)</span><span class="sxs-lookup"><span data-stu-id="50551-125">public void AOTSetImage(Image image)</span></span>                                     |             |

## <a name="method-aotgetdata"></a><span data-ttu-id="50551-126">メソッド AOTGetData</span><span class="sxs-lookup"><span data-stu-id="50551-126">Method AOTGetData</span></span>

```xpp
public BinData AOTGetData()
```

### <a name="return-value---aotgetdata"></a><span data-ttu-id="50551-127">戻り値 - AOTGetData</span><span class="sxs-lookup"><span data-stu-id="50551-127">Return Value - AOTGetData</span></span>

## <a name="method-aotgetimage"></a><span data-ttu-id="50551-128">メソッド AOTGetImage</span><span class="sxs-lookup"><span data-stu-id="50551-128">Method AOTGetImage</span></span>

```xpp
public Image AOTGetImage()
```

### <a name="return-value---aotgetimage"></a><span data-ttu-id="50551-129">戻り値 - AOTGetImage</span><span class="sxs-lookup"><span data-stu-id="50551-129">Return Value - AOTGetImage</span></span>

## <a name="method-changedby"></a><span data-ttu-id="50551-130">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="50551-130">Method changedBy</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="50551-131">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="50551-131">Parameters - changedBy</span></span>

<span data-ttu-id="50551-132">値</span><span class="sxs-lookup"><span data-stu-id="50551-132">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="50551-133">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="50551-133">Return Value - changedBy</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="50551-134">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="50551-134">Method changedDate</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="50551-135">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="50551-135">Parameters - changedDate</span></span>

<span data-ttu-id="50551-136">値</span><span class="sxs-lookup"><span data-stu-id="50551-136">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="50551-137">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="50551-137">Return Value - changedDate</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="50551-138">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="50551-138">Method changedTime</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="50551-139">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="50551-139">Parameters - changedTime</span></span>

<span data-ttu-id="50551-140">値</span><span class="sxs-lookup"><span data-stu-id="50551-140">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="50551-141">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="50551-141">Return Value - changedTime</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="50551-142">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="50551-142">Method configurationKey</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="50551-143">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="50551-143">Parameters - configurationKey</span></span>

<span data-ttu-id="50551-144">値</span><span class="sxs-lookup"><span data-stu-id="50551-144">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="50551-145">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="50551-145">Return Value - configurationKey</span></span>

## <a name="method-createdby"></a><span data-ttu-id="50551-146">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="50551-146">Method createdBy</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="50551-147">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="50551-147">Parameters - createdBy</span></span>

<span data-ttu-id="50551-148">値</span><span class="sxs-lookup"><span data-stu-id="50551-148">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="50551-149">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="50551-149">Return Value - createdBy</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="50551-150">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="50551-150">Method creationDate</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="50551-151">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="50551-151">Parameters - creationDate</span></span>

<span data-ttu-id="50551-152">値</span><span class="sxs-lookup"><span data-stu-id="50551-152">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="50551-153">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="50551-153">Return Value - creationDate</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="50551-154">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="50551-154">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="50551-155">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="50551-155">Parameters - creationTime</span></span>

<span data-ttu-id="50551-156">値</span><span class="sxs-lookup"><span data-stu-id="50551-156">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="50551-157">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="50551-157">Return Value - creationTime</span></span>

## <a name="method-filename"></a><span data-ttu-id="50551-158">メソッド filename</span><span class="sxs-lookup"><span data-stu-id="50551-158">Method filename</span></span>

```xpp
public str filename([str value])
```

### <a name="parameters---filename"></a><span data-ttu-id="50551-159">パラメーター - filename</span><span class="sxs-lookup"><span data-stu-id="50551-159">Parameters - filename</span></span>

<span data-ttu-id="50551-160">値</span><span class="sxs-lookup"><span data-stu-id="50551-160">value</span></span>  

### <a name="return-value---filename"></a><span data-ttu-id="50551-161">戻り値 - filename</span><span class="sxs-lookup"><span data-stu-id="50551-161">Return Value - filename</span></span>

## <a name="method-helptext"></a><span data-ttu-id="50551-162">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="50551-162">Method helpText</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="50551-163">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="50551-163">Parameters - helpText</span></span>

<span data-ttu-id="50551-164">値</span><span class="sxs-lookup"><span data-stu-id="50551-164">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="50551-165">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="50551-165">Return Value - helpText</span></span>

## <a name="method-label"></a><span data-ttu-id="50551-166">メソッド label</span><span class="sxs-lookup"><span data-stu-id="50551-166">Method label</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="50551-167">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="50551-167">Parameters - label</span></span>

<span data-ttu-id="50551-168">値</span><span class="sxs-lookup"><span data-stu-id="50551-168">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="50551-169">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="50551-169">Return Value - label</span></span>

## <a name="method-name"></a><span data-ttu-id="50551-170">メソッド名</span><span class="sxs-lookup"><span data-stu-id="50551-170">Method name</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="50551-171">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="50551-171">Parameters - name</span></span>

<span data-ttu-id="50551-172">値</span><span class="sxs-lookup"><span data-stu-id="50551-172">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="50551-173">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="50551-173">Return Value - name</span></span>

## <a name="method-origin"></a><span data-ttu-id="50551-174">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="50551-174">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="50551-175">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="50551-175">Parameters - origin</span></span>

<span data-ttu-id="50551-176">値</span><span class="sxs-lookup"><span data-stu-id="50551-176">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="50551-177">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="50551-177">Return Value - origin</span></span>

## <a name="method-aotcreateimage"></a><span data-ttu-id="50551-178">メソッド AOTCreateImage</span><span class="sxs-lookup"><span data-stu-id="50551-178">Method AOTCreateImage</span></span>

```xpp
public static Image AOTCreateImage(str imageName)
```

### <a name="parameters---aotcreateimage"></a><span data-ttu-id="50551-179">パラメーター - AOTCreateImage</span><span class="sxs-lookup"><span data-stu-id="50551-179">Parameters - AOTCreateImage</span></span>

<span data-ttu-id="50551-180">imageName</span><span class="sxs-lookup"><span data-stu-id="50551-180">imageName</span></span>  

### <a name="return-value---aotcreateimage"></a><span data-ttu-id="50551-181">戻り値 - AOTCreateImage</span><span class="sxs-lookup"><span data-stu-id="50551-181">Return Value - AOTCreateImage</span></span>

## <a name="method-aotsetdata"></a><span data-ttu-id="50551-182">メソッド AOTSetData</span><span class="sxs-lookup"><span data-stu-id="50551-182">Method AOTSetData</span></span>

```xpp
public void AOTSetData(BinData data)
```

### <a name="parameters---aotsetdata"></a><span data-ttu-id="50551-183">パラメーター - AOTSetData</span><span class="sxs-lookup"><span data-stu-id="50551-183">Parameters - AOTSetData</span></span>

<span data-ttu-id="50551-184">データ</span><span class="sxs-lookup"><span data-stu-id="50551-184">data</span></span>  

## <a name="method-aotsetimage"></a><span data-ttu-id="50551-185">メソッド AOTSetImage</span><span class="sxs-lookup"><span data-stu-id="50551-185">Method AOTSetImage</span></span>

```xpp
public void AOTSetImage(Image image)
```

### <a name="parameters---aotsetimage"></a><span data-ttu-id="50551-186">パラメーター - AOTSetImage</span><span class="sxs-lookup"><span data-stu-id="50551-186">Parameters - AOTSetImage</span></span>

<span data-ttu-id="50551-187">画像</span><span class="sxs-lookup"><span data-stu-id="50551-187">image</span></span>  

