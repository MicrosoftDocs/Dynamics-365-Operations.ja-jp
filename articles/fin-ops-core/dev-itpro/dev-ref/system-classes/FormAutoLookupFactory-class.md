---
title: FormAutoLookupFactory クラス
description: このトピックでは、FormAutoLookupFactory クラスについて説明します。
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
ms.openlocfilehash: 7f5ca8d7d0cbc3a555d58b6b0d3d0cd93a7f0d65
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502661"
---
# <a name="class-formautolookupfactory"></a><span data-ttu-id="9db38-103">クラス FormAutoLookupFactory</span><span class="sxs-lookup"><span data-stu-id="9db38-103">Class FormAutoLookupFactory</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormAutoLookupFactory extends FieldBinding
```

## <a name="remarks"></a><span data-ttu-id="9db38-104">備考</span><span class="sxs-lookup"><span data-stu-id="9db38-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="9db38-105">例</span><span class="sxs-lookup"><span data-stu-id="9db38-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="9db38-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="9db38-106">Methods</span></span>

| <span data-ttu-id="9db38-107">方法</span><span class="sxs-lookup"><span data-stu-id="9db38-107">Method</span></span>                                                                                                                                                                              | <span data-ttu-id="9db38-108">説明</span><span class="sxs-lookup"><span data-stu-id="9db38-108">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9db38-109">::public static xFormRun buildLookupFormByField (FormControl controlHostingLookup, FieldBinding fieldBinding)</span><span class="sxs-lookup"><span data-stu-id="9db38-109">::public static xFormRun buildLookupFormByField(FormControl controlHostingLookup, FieldBinding fieldBinding)</span></span>                                                                        |                                                                |
| <span data-ttu-id="9db38-110">::public static xFormRun buildLookupFromCustomForm (FormControl controlHostingLookup, Form customLookupForm, FieldBinding fieldBinding, \[xArgs customArgs\], \[Query customQuery\])</span><span class="sxs-lookup"><span data-stu-id="9db38-110">::public static xFormRun buildLookupFromCustomForm(FormControl controlHostingLookup, Form customLookupForm, FieldBinding fieldBinding, \[xArgs customArgs\], \[Query customQuery\])</span></span> |                                                                |
| <span data-ttu-id="9db38-111">::public static xFormRun buildReferenceLookupFromCustomForm (FormReferenceControl referenceControlHostingLookup, Form customLookupForm, \[xArgs customArgs\], \[Query customQuery\])</span><span class="sxs-lookup"><span data-stu-id="9db38-111">::public static xFormRun buildReferenceLookupFromCustomForm(FormReferenceControl referenceControlHostingLookup, Form customLookupForm, \[xArgs customArgs\], \[Query customQuery\])</span></span> |                                                                |
| <span data-ttu-id="9db38-112">::public static void createLookupForClientsideControl (xFormRun parentForm, str targetId, str controlName, int tableId, int fieldId, str controlValue, boolean isInFilterMode)</span><span class="sxs-lookup"><span data-stu-id="9db38-112">::public static void createLookupForClientsideControl(xFormRun parentForm, str targetId, str controlName, int tableId, int fieldId, str controlValue, boolean isInFilterMode)</span></span>       |                                                                |
| <span data-ttu-id="9db38-113">::public static void performFormLookup(xFormRun lookupForm, \[boolean blockUntilLookupClosed\], \[FormControl controlHostingLookup\])</span><span class="sxs-lookup"><span data-stu-id="9db38-113">::public static void performFormLookup(xFormRun lookupForm, \[boolean blockUntilLookupClosed\], \[FormControl controlHostingLookup\])</span></span>                                               |                                                                |
| <span data-ttu-id="9db38-114">private void new()</span><span class="sxs-lookup"><span data-stu-id="9db38-114">private void new()</span></span>                                                                                                                                                                  | <span data-ttu-id="9db38-115">FormAutoLookupFactory クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9db38-115">Initializes a new instance of the FormAutoLookupFactory class.</span></span> |

## <a name="method-buildlookupformbyfield"></a><span data-ttu-id="9db38-116">メソッド buildLookupFormByField</span><span class="sxs-lookup"><span data-stu-id="9db38-116">Method buildLookupFormByField</span></span>

```xpp
public static xFormRun buildLookupFormByField(FormControl controlHostingLookup, FieldBinding fieldBinding)
```

### <a name="parameters---buildlookupformbyfield"></a><span data-ttu-id="9db38-117">パラメーター - buildLookupFormByField</span><span class="sxs-lookup"><span data-stu-id="9db38-117">Parameters - buildLookupFormByField</span></span>

<span data-ttu-id="9db38-118">controlHostingLookup</span><span class="sxs-lookup"><span data-stu-id="9db38-118">controlHostingLookup</span></span>  

<!-- -->

<span data-ttu-id="9db38-119">fieldBinding</span><span class="sxs-lookup"><span data-stu-id="9db38-119">fieldBinding</span></span>  

### <a name="return-value---buildlookupformbyfield"></a><span data-ttu-id="9db38-120">戻り値 - buildLookupFormByField</span><span class="sxs-lookup"><span data-stu-id="9db38-120">Return Value - buildLookupFormByField</span></span>

## <a name="method-buildlookupfromcustomform"></a><span data-ttu-id="9db38-121">メソッド buildLookupFromCustomForm</span><span class="sxs-lookup"><span data-stu-id="9db38-121">Method buildLookupFromCustomForm</span></span>

```xpp
public static xFormRun buildLookupFromCustomForm(FormControl controlHostingLookup, Form customLookupForm, FieldBinding fieldBinding, [xArgs customArgs], [Query customQuery])
```

### <a name="parameters---buildlookupfromcustomform"></a><span data-ttu-id="9db38-122">パラメーター - buildLookupFromCustomForm</span><span class="sxs-lookup"><span data-stu-id="9db38-122">Parameters - buildLookupFromCustomForm</span></span>

<span data-ttu-id="9db38-123">controlHostingLookup</span><span class="sxs-lookup"><span data-stu-id="9db38-123">controlHostingLookup</span></span>  

<!-- -->

<span data-ttu-id="9db38-124">customLookupForm</span><span class="sxs-lookup"><span data-stu-id="9db38-124">customLookupForm</span></span>  

<!-- -->

<span data-ttu-id="9db38-125">fieldBinding</span><span class="sxs-lookup"><span data-stu-id="9db38-125">fieldBinding</span></span>  

<!-- -->

<span data-ttu-id="9db38-126">customArgs</span><span class="sxs-lookup"><span data-stu-id="9db38-126">customArgs</span></span>  

<!-- -->

<span data-ttu-id="9db38-127">customQuery</span><span class="sxs-lookup"><span data-stu-id="9db38-127">customQuery</span></span>  

### <a name="return-value---buildlookupfromcustomform"></a><span data-ttu-id="9db38-128">戻り値 - buildLookupFromCustomForm</span><span class="sxs-lookup"><span data-stu-id="9db38-128">Return Value - buildLookupFromCustomForm</span></span>

## <a name="method-buildreferencelookupfromcustomform"></a><span data-ttu-id="9db38-129">メソッド buildReferenceLookupFromCustomForm</span><span class="sxs-lookup"><span data-stu-id="9db38-129">Method buildReferenceLookupFromCustomForm</span></span>

```xpp
public static xFormRun buildReferenceLookupFromCustomForm(FormReferenceControl referenceControlHostingLookup, Form customLookupForm, [xArgs customArgs], [Query customQuery])
```

### <a name="parameters---buildreferencelookupfromcustomform"></a><span data-ttu-id="9db38-130">パラメーター - buildReferenceLookupFromCustomForm</span><span class="sxs-lookup"><span data-stu-id="9db38-130">Parameters - buildReferenceLookupFromCustomForm</span></span>

<span data-ttu-id="9db38-131">referenceControlHostingLookup</span><span class="sxs-lookup"><span data-stu-id="9db38-131">referenceControlHostingLookup</span></span>  

<!-- -->

<span data-ttu-id="9db38-132">customLookupForm</span><span class="sxs-lookup"><span data-stu-id="9db38-132">customLookupForm</span></span>  

<!-- -->

<span data-ttu-id="9db38-133">customArgs</span><span class="sxs-lookup"><span data-stu-id="9db38-133">customArgs</span></span>  

<!-- -->

<span data-ttu-id="9db38-134">customQuery</span><span class="sxs-lookup"><span data-stu-id="9db38-134">customQuery</span></span>  

### <a name="return-value---buildreferencelookupfromcustomform"></a><span data-ttu-id="9db38-135">戻り値 - buildReferenceLookupFromCustomForm</span><span class="sxs-lookup"><span data-stu-id="9db38-135">Return Value - buildReferenceLookupFromCustomForm</span></span>

## <a name="method-createlookupforclientsidecontrol"></a><span data-ttu-id="9db38-136">メソッド createLookupForClientsideControl</span><span class="sxs-lookup"><span data-stu-id="9db38-136">Method createLookupForClientsideControl</span></span>

```xpp
public static void createLookupForClientsideControl(xFormRun parentForm, str targetId, str controlName, int tableId, int fieldId, str controlValue, boolean isInFilterMode)
```

### <a name="parameters---createlookupforclientsidecontrol"></a><span data-ttu-id="9db38-137">パラメーター - createLookupForClientsideControl</span><span class="sxs-lookup"><span data-stu-id="9db38-137">Parameters - createLookupForClientsideControl</span></span>

<span data-ttu-id="9db38-138">parentForm</span><span class="sxs-lookup"><span data-stu-id="9db38-138">parentForm</span></span>  

<!-- -->

<span data-ttu-id="9db38-139">targetId</span><span class="sxs-lookup"><span data-stu-id="9db38-139">targetId</span></span>  

<!-- -->

<span data-ttu-id="9db38-140">controlName</span><span class="sxs-lookup"><span data-stu-id="9db38-140">controlName</span></span>  

<!-- -->

<span data-ttu-id="9db38-141">tableId</span><span class="sxs-lookup"><span data-stu-id="9db38-141">tableId</span></span>  

<!-- -->

<span data-ttu-id="9db38-142">fieldId</span><span class="sxs-lookup"><span data-stu-id="9db38-142">fieldId</span></span>  

<!-- -->

<span data-ttu-id="9db38-143">controlValue</span><span class="sxs-lookup"><span data-stu-id="9db38-143">controlValue</span></span>  

<!-- -->

<span data-ttu-id="9db38-144">isInFilterMode</span><span class="sxs-lookup"><span data-stu-id="9db38-144">isInFilterMode</span></span>  

## <a name="method-performformlookup"></a><span data-ttu-id="9db38-145">メソッド performFormLookup</span><span class="sxs-lookup"><span data-stu-id="9db38-145">Method performFormLookup</span></span>

```xpp
public static void performFormLookup(xFormRun lookupForm, [boolean blockUntilLookupClosed], [FormControl controlHostingLookup])
```

### <a name="parameters---performformlookup"></a><span data-ttu-id="9db38-146">パラメーター - performFormLookup</span><span class="sxs-lookup"><span data-stu-id="9db38-146">Parameters - performFormLookup</span></span>

<span data-ttu-id="9db38-147">lookupForm</span><span class="sxs-lookup"><span data-stu-id="9db38-147">lookupForm</span></span>  

<!-- -->

<span data-ttu-id="9db38-148">blockUntilLookupClosed</span><span class="sxs-lookup"><span data-stu-id="9db38-148">blockUntilLookupClosed</span></span>  

<!-- -->

<span data-ttu-id="9db38-149">controlHostingLookup</span><span class="sxs-lookup"><span data-stu-id="9db38-149">controlHostingLookup</span></span>  

## <a name="method-new"></a><span data-ttu-id="9db38-150">メソッド new</span><span class="sxs-lookup"><span data-stu-id="9db38-150">Method new</span></span>

<span data-ttu-id="9db38-151">FormAutoLookupFactory クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9db38-151">Initializes a new instance of the FormAutoLookupFactory class.</span></span>

```xpp
private void new()
```

