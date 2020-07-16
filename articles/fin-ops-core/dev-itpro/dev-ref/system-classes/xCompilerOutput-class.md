---
title: xCompilerOutput クラス
description: このトピックでは、xCompilerOutput クラスについて説明します。
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
ms.openlocfilehash: 8f572c5bcc139b85b26e627fee161356cf759145
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502765"
---
# <a name="class-xcompileroutput"></a><span data-ttu-id="32990-103">クラス xCompilerOutput</span><span class="sxs-lookup"><span data-stu-id="32990-103">Class xCompilerOutput</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xCompilerOutput extends Object
```

## <a name="remarks"></a><span data-ttu-id="32990-104">備考</span><span class="sxs-lookup"><span data-stu-id="32990-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="32990-105">例</span><span class="sxs-lookup"><span data-stu-id="32990-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="32990-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="32990-106">Methods</span></span>

| <span data-ttu-id="32990-107">方法</span><span class="sxs-lookup"><span data-stu-id="32990-107">Method</span></span>                                                                                                                         | <span data-ttu-id="32990-108">説明</span><span class="sxs-lookup"><span data-stu-id="32990-108">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="32990-109">public str getErrorMessage(int errorCode, int severity, str errorString)</span><span class="sxs-lookup"><span data-stu-id="32990-109">public str getErrorMessage(int errorCode, int severity, str errorString)</span></span>                                                       |                                                          |
| <span data-ttu-id="32990-110">public container getSquiggleInfo(str treeNodePath)</span><span class="sxs-lookup"><span data-stu-id="32990-110">public container getSquiggleInfo(str treeNodePath)</span></span>                                                                             |                                                          |
| <span data-ttu-id="32990-111">public void compilerStatus(UtilElementType utilElementType, str utilElementName)</span><span class="sxs-lookup"><span data-stu-id="32990-111">public void compilerStatus(UtilElementType utilElementType, str utilElementName)</span></span>                                               |                                                          |
| <span data-ttu-id="32990-112">public void setActiveTab(int tab)</span><span class="sxs-lookup"><span data-stu-id="32990-112">public void setActiveTab(int tab)</span></span>                                                                                              |                                                          |
| <span data-ttu-id="32990-113">public void startCompilationObject(str path)</span><span class="sxs-lookup"><span data-stu-id="32990-113">public void startCompilationObject(str path)</span></span>                                                                                   |                                                          |
| <span data-ttu-id="32990-114">public void endCompilation()</span><span class="sxs-lookup"><span data-stu-id="32990-114">public void endCompilation()</span></span>                                                                                                   |                                                          |
| <span data-ttu-id="32990-115">public void startExport()</span><span class="sxs-lookup"><span data-stu-id="32990-115">public void startExport()</span></span>                                                                                                      |                                                          |
| <span data-ttu-id="32990-116">public void startCompilation(int flag, str path, int activeWindowHandle)</span><span class="sxs-lookup"><span data-stu-id="32990-116">public void startCompilation(int flag, str path, int activeWindowHandle)</span></span>                                                       |                                                          |
| <span data-ttu-id="32990-117">public void importOutput(str buffer)</span><span class="sxs-lookup"><span data-stu-id="32990-117">public void importOutput(str buffer)</span></span>                                                                                           |                                                          |
| <span data-ttu-id="32990-118">public void endExport()</span><span class="sxs-lookup"><span data-stu-id="32990-118">public void endExport()</span></span>                                                                                                        |                                                          |
| <span data-ttu-id="32990-119">public void endCompilationObject(str path)</span><span class="sxs-lookup"><span data-stu-id="32990-119">public void endCompilationObject(str path)</span></span>                                                                                     |                                                          |
| <span data-ttu-id="32990-120">public void startImport()</span><span class="sxs-lookup"><span data-stu-id="32990-120">public void startImport()</span></span>                                                                                                      |                                                          |
| <span data-ttu-id="32990-121">public void new()</span><span class="sxs-lookup"><span data-stu-id="32990-121">public void new()</span></span>                                                                                                              | <span data-ttu-id="32990-122">xCompilerOutput クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="32990-122">Initializes a new instance of the xCompilerOutput class.</span></span> |
| <span data-ttu-id="32990-123">public void compilerOutputMessage(str path, int errorCode, int line, int col, int severity, str errorString, str propertyName)</span><span class="sxs-lookup"><span data-stu-id="32990-123">public void compilerOutputMessage(str path, int errorCode, int line, int col, int severity, str errorString, str propertyName)</span></span> |                                                          |
| <span data-ttu-id="32990-124">public void exportOutput(str buffer)</span><span class="sxs-lookup"><span data-stu-id="32990-124">public void exportOutput(str buffer)</span></span>                                                                                           |                                                          |
| <span data-ttu-id="32990-125">public void endCILGenerationOutput()</span><span class="sxs-lookup"><span data-stu-id="32990-125">public void endCILGenerationOutput()</span></span>                                                                                           |                                                          |
| <span data-ttu-id="32990-126">public void cilGenerationOutput(str msg, str path, int severity, int line, int col)</span><span class="sxs-lookup"><span data-stu-id="32990-126">public void cilGenerationOutput(str msg, str path, int severity, int line, int col)</span></span>                                            |                                                          |
| <span data-ttu-id="32990-127">public void endImport()</span><span class="sxs-lookup"><span data-stu-id="32990-127">public void endImport()</span></span>                                                                                                        |                                                          |
| <span data-ttu-id="32990-128">public void nextError()</span><span class="sxs-lookup"><span data-stu-id="32990-128">public void nextError()</span></span>                                                                                                        |                                                          |
| <span data-ttu-id="32990-129">public void startCILGenerationOutput()</span><span class="sxs-lookup"><span data-stu-id="32990-129">public void startCILGenerationOutput()</span></span>                                                                                         |                                                          |

## <a name="method-geterrormessage"></a><span data-ttu-id="32990-130">メソッド getErrorMessage</span><span class="sxs-lookup"><span data-stu-id="32990-130">Method getErrorMessage</span></span>

```xpp
public str getErrorMessage(int errorCode, int severity, str errorString)
```

### <a name="parameters---geterrormessage"></a><span data-ttu-id="32990-131">パラメーター - getErrorMessage</span><span class="sxs-lookup"><span data-stu-id="32990-131">Parameters - getErrorMessage</span></span>

<span data-ttu-id="32990-132">errorCode</span><span class="sxs-lookup"><span data-stu-id="32990-132">errorCode</span></span>  

<!-- -->

<span data-ttu-id="32990-133">severity</span><span class="sxs-lookup"><span data-stu-id="32990-133">severity</span></span>  

<!-- -->

<span data-ttu-id="32990-134">errorString</span><span class="sxs-lookup"><span data-stu-id="32990-134">errorString</span></span>  

### <a name="return-value---geterrormessage"></a><span data-ttu-id="32990-135">戻り値 - getErrorMessage</span><span class="sxs-lookup"><span data-stu-id="32990-135">Return Value - getErrorMessage</span></span>

## <a name="method-getsquiggleinfo"></a><span data-ttu-id="32990-136">メソッド getSquiggleInfo</span><span class="sxs-lookup"><span data-stu-id="32990-136">Method getSquiggleInfo</span></span>

```xpp
public container getSquiggleInfo(str treeNodePath)
```

### <a name="parameters---getsquiggleinfo"></a><span data-ttu-id="32990-137">パラメーター - getSquiggleInfo</span><span class="sxs-lookup"><span data-stu-id="32990-137">Parameters - getSquiggleInfo</span></span>

<span data-ttu-id="32990-138">treeNodePath</span><span class="sxs-lookup"><span data-stu-id="32990-138">treeNodePath</span></span>  

### <a name="return-value---getsquiggleinfo"></a><span data-ttu-id="32990-139">戻り値 - getSquiggleInfo</span><span class="sxs-lookup"><span data-stu-id="32990-139">Return Value - getSquiggleInfo</span></span>

## <a name="method-compilerstatus"></a><span data-ttu-id="32990-140">メソッド compilerStatus</span><span class="sxs-lookup"><span data-stu-id="32990-140">Method compilerStatus</span></span>

```xpp
public void compilerStatus(UtilElementType utilElementType, str utilElementName)
```

### <a name="parameters---compilerstatus"></a><span data-ttu-id="32990-141">パラメーター - compilerStatus</span><span class="sxs-lookup"><span data-stu-id="32990-141">Parameters - compilerStatus</span></span>

<span data-ttu-id="32990-142">utilElementType</span><span class="sxs-lookup"><span data-stu-id="32990-142">utilElementType</span></span>  

<!-- -->

<span data-ttu-id="32990-143">utilElementName</span><span class="sxs-lookup"><span data-stu-id="32990-143">utilElementName</span></span>  

## <a name="method-setactivetab"></a><span data-ttu-id="32990-144">メソッド setActiveTab</span><span class="sxs-lookup"><span data-stu-id="32990-144">Method setActiveTab</span></span>

```xpp
public void setActiveTab(int tab)
```

### <a name="parameters---setactivetab"></a><span data-ttu-id="32990-145">パラメーター - setActiveTab</span><span class="sxs-lookup"><span data-stu-id="32990-145">Parameters - setActiveTab</span></span>

<span data-ttu-id="32990-146">tab</span><span class="sxs-lookup"><span data-stu-id="32990-146">tab</span></span>  

## <a name="method-startcompilationobject"></a><span data-ttu-id="32990-147">メソッド startCompilationObject</span><span class="sxs-lookup"><span data-stu-id="32990-147">Method startCompilationObject</span></span>

```xpp
public void startCompilationObject(str path)
```

### <a name="parameters---startcompilationobject"></a><span data-ttu-id="32990-148">パラメーター - startCompilationObject</span><span class="sxs-lookup"><span data-stu-id="32990-148">Parameters - startCompilationObject</span></span>

<span data-ttu-id="32990-149">path</span><span class="sxs-lookup"><span data-stu-id="32990-149">path</span></span>  

## <a name="method-endcompilation"></a><span data-ttu-id="32990-150">メソッド endCompilation</span><span class="sxs-lookup"><span data-stu-id="32990-150">Method endCompilation</span></span>

```xpp
public void endCompilation()
```

## <a name="method-startexport"></a><span data-ttu-id="32990-151">メソッド startExport</span><span class="sxs-lookup"><span data-stu-id="32990-151">Method startExport</span></span>

```xpp
public void startExport()
```

## <a name="method-startcompilation"></a><span data-ttu-id="32990-152">メソッド startCompilation</span><span class="sxs-lookup"><span data-stu-id="32990-152">Method startCompilation</span></span>

```xpp
public void startCompilation(int flag, str path, int activeWindowHandle)
```

### <a name="parameters---startcompilation"></a><span data-ttu-id="32990-153">パラメーター - startCompilation</span><span class="sxs-lookup"><span data-stu-id="32990-153">Parameters - startCompilation</span></span>

<span data-ttu-id="32990-154">flag</span><span class="sxs-lookup"><span data-stu-id="32990-154">flag</span></span>  

<!-- -->

<span data-ttu-id="32990-155">path</span><span class="sxs-lookup"><span data-stu-id="32990-155">path</span></span>  

<!-- -->

<span data-ttu-id="32990-156">activeWindowHandle</span><span class="sxs-lookup"><span data-stu-id="32990-156">activeWindowHandle</span></span>  

## <a name="method-importoutput"></a><span data-ttu-id="32990-157">メソッド importOutput</span><span class="sxs-lookup"><span data-stu-id="32990-157">Method importOutput</span></span>

```xpp
public void importOutput(str buffer)
```

### <a name="parameters---importoutput"></a><span data-ttu-id="32990-158">パラメーター - importOutput</span><span class="sxs-lookup"><span data-stu-id="32990-158">Parameters - importOutput</span></span>

<span data-ttu-id="32990-159">バッファ</span><span class="sxs-lookup"><span data-stu-id="32990-159">buffer</span></span>  

## <a name="method-endexport"></a><span data-ttu-id="32990-160">メソッド endExport</span><span class="sxs-lookup"><span data-stu-id="32990-160">Method endExport</span></span>

```xpp
public void endExport()
```

## <a name="method-endcompilationobject"></a><span data-ttu-id="32990-161">メソッド endCompilationObject</span><span class="sxs-lookup"><span data-stu-id="32990-161">Method endCompilationObject</span></span>

```xpp
public void endCompilationObject(str path)
```

### <a name="parameters---endcompilationobject"></a><span data-ttu-id="32990-162">パラメーター - endCompilationObject</span><span class="sxs-lookup"><span data-stu-id="32990-162">Parameters - endCompilationObject</span></span>

<span data-ttu-id="32990-163">path</span><span class="sxs-lookup"><span data-stu-id="32990-163">path</span></span>  

## <a name="method-startimport"></a><span data-ttu-id="32990-164">メソッド startImport</span><span class="sxs-lookup"><span data-stu-id="32990-164">Method startImport</span></span>

```xpp
public void startImport()
```

## <a name="method-new"></a><span data-ttu-id="32990-165">メソッド new</span><span class="sxs-lookup"><span data-stu-id="32990-165">Method new</span></span>

<span data-ttu-id="32990-166">xCompilerOutput クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="32990-166">Initializes a new instance of the xCompilerOutput class.</span></span>

```xpp
public void new()
```

## <a name="method-compileroutputmessage"></a><span data-ttu-id="32990-167">メソッド compilerOutputMessage</span><span class="sxs-lookup"><span data-stu-id="32990-167">Method compilerOutputMessage</span></span>

```xpp
public void compilerOutputMessage(str path, int errorCode, int line, int col, int severity, str errorString, str propertyName)
```

### <a name="parameters---compileroutputmessage"></a><span data-ttu-id="32990-168">パラメーター - compilerOutputMessage</span><span class="sxs-lookup"><span data-stu-id="32990-168">Parameters - compilerOutputMessage</span></span>

<span data-ttu-id="32990-169">path</span><span class="sxs-lookup"><span data-stu-id="32990-169">path</span></span>  

<!-- -->

<span data-ttu-id="32990-170">errorCode</span><span class="sxs-lookup"><span data-stu-id="32990-170">errorCode</span></span>  

<!-- -->

<span data-ttu-id="32990-171">明細行</span><span class="sxs-lookup"><span data-stu-id="32990-171">line</span></span>  

<!-- -->

<span data-ttu-id="32990-172">col</span><span class="sxs-lookup"><span data-stu-id="32990-172">col</span></span>  

<!-- -->

<span data-ttu-id="32990-173">severity</span><span class="sxs-lookup"><span data-stu-id="32990-173">severity</span></span>  

<!-- -->

<span data-ttu-id="32990-174">errorString</span><span class="sxs-lookup"><span data-stu-id="32990-174">errorString</span></span>  

<!-- -->

<span data-ttu-id="32990-175">propertyName</span><span class="sxs-lookup"><span data-stu-id="32990-175">propertyName</span></span>  

## <a name="method-exportoutput"></a><span data-ttu-id="32990-176">メソッド exportOutput</span><span class="sxs-lookup"><span data-stu-id="32990-176">Method exportOutput</span></span>

```xpp
public void exportOutput(str buffer)
```

### <a name="parameters---exportoutput"></a><span data-ttu-id="32990-177">パラメーター - exportOutput</span><span class="sxs-lookup"><span data-stu-id="32990-177">Parameters - exportOutput</span></span>

<span data-ttu-id="32990-178">バッファ</span><span class="sxs-lookup"><span data-stu-id="32990-178">buffer</span></span>  

## <a name="method-endcilgenerationoutput"></a><span data-ttu-id="32990-179">メソッド endCILGenerationOutput</span><span class="sxs-lookup"><span data-stu-id="32990-179">Method endCILGenerationOutput</span></span>

```xpp
public void endCILGenerationOutput()
```

## <a name="method-cilgenerationoutput"></a><span data-ttu-id="32990-180">メソッド cilGenerationOutput</span><span class="sxs-lookup"><span data-stu-id="32990-180">Method cilGenerationOutput</span></span>

```xpp
public void cilGenerationOutput(str msg, str path, int severity, int line, int col)
```

### <a name="parameters---cilgenerationoutput"></a><span data-ttu-id="32990-181">パラメーター - cilGenerationOutput</span><span class="sxs-lookup"><span data-stu-id="32990-181">Parameters - cilGenerationOutput</span></span>

<span data-ttu-id="32990-182">msg</span><span class="sxs-lookup"><span data-stu-id="32990-182">msg</span></span>  

<!-- -->

<span data-ttu-id="32990-183">path</span><span class="sxs-lookup"><span data-stu-id="32990-183">path</span></span>  

<!-- -->

<span data-ttu-id="32990-184">severity</span><span class="sxs-lookup"><span data-stu-id="32990-184">severity</span></span>  

<!-- -->

<span data-ttu-id="32990-185">明細行</span><span class="sxs-lookup"><span data-stu-id="32990-185">line</span></span>  

<!-- -->

<span data-ttu-id="32990-186">col</span><span class="sxs-lookup"><span data-stu-id="32990-186">col</span></span>  

## <a name="method-endimport"></a><span data-ttu-id="32990-187">メソッド endImport</span><span class="sxs-lookup"><span data-stu-id="32990-187">Method endImport</span></span>

```xpp
public void endImport()
```

## <a name="method-nexterror"></a><span data-ttu-id="32990-188">メソッド nextError</span><span class="sxs-lookup"><span data-stu-id="32990-188">Method nextError</span></span>

```xpp
public void nextError()
```

## <a name="method-startcilgenerationoutput"></a><span data-ttu-id="32990-189">メソッド startCILGenerationOutput</span><span class="sxs-lookup"><span data-stu-id="32990-189">Method startCILGenerationOutput</span></span>

```xpp
public void startCILGenerationOutput()
```

