---
title: DictConfigurationKey クラス
description: このトピックでは、DictConfigurationKey クラスについて説明します。
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
ms.openlocfilehash: 197a150a8076ed969254a23cca7e5edce56f9a52
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502993"
---
# <a name="class-dictconfigurationkey"></a><span data-ttu-id="b7fba-103">クラス DictConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="b7fba-103">Class DictConfigurationKey</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictConfigurationKey extends Object
```

<span data-ttu-id="b7fba-104">DictConfigurationKey クラスは、コンフィギュレーション キーの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-104">The DictConfigurationKey class provides information about a configuration key.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7fba-105">備考</span><span class="sxs-lookup"><span data-stu-id="b7fba-105">Remarks</span></span>

<span data-ttu-id="b7fba-106">DictConfigurationKey クラスを使用する例については、新しいメソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7fba-106">For an example that uses the DictConfigurationKey class, see the new method.</span></span>

## <a name="examples"></a><span data-ttu-id="b7fba-107">例</span><span class="sxs-lookup"><span data-stu-id="b7fba-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b7fba-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="b7fba-108">Methods</span></span>

| <span data-ttu-id="b7fba-109">方法</span><span class="sxs-lookup"><span data-stu-id="b7fba-109">Method</span></span>                                                                     | <span data-ttu-id="b7fba-110">説明</span><span class="sxs-lookup"><span data-stu-id="b7fba-110">Description</span></span>                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="b7fba-111">public boolean enabled()</span><span class="sxs-lookup"><span data-stu-id="b7fba-111">public boolean enabled()</span></span>                                                   | <span data-ttu-id="b7fba-112">構成キーが有効かどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-112">Returns a value that indicates whether the configuration key is enabled.</span></span>  |
| <span data-ttu-id="b7fba-113">public ConfigurationKeyId id()</span><span class="sxs-lookup"><span data-stu-id="b7fba-113">public ConfigurationKeyId id()</span></span>                                             | <span data-ttu-id="b7fba-114">コンフィギュレーション キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-114">Returns the ID of the configuration key.</span></span>                                  |
| <span data-ttu-id="b7fba-115">public str label()</span><span class="sxs-lookup"><span data-stu-id="b7fba-115">public str label()</span></span>                                                         | <span data-ttu-id="b7fba-116">コンフィギュレーション キーのラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-116">Returns the label for a configuration key.</span></span>                                |
| <span data-ttu-id="b7fba-117">public str labelId()</span><span class="sxs-lookup"><span data-stu-id="b7fba-117">public str labelId()</span></span>                                                       |                                                                           |
| <span data-ttu-id="b7fba-118">public LicenseCodeId licenseCode()</span><span class="sxs-lookup"><span data-stu-id="b7fba-118">public LicenseCodeId licenseCode()</span></span>                                         | <span data-ttu-id="b7fba-119">コンフィギュレーション キーのライセンス コード ID を返します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-119">Returns the license code ID for the configuration key.</span></span>                    |
| <span data-ttu-id="b7fba-120">public str name()</span><span class="sxs-lookup"><span data-stu-id="b7fba-120">public str name()</span></span>                                                          | <span data-ttu-id="b7fba-121">コンフィギュレーション キーの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-121">Returns the name of the configuration key.</span></span>                                |
| <span data-ttu-id="b7fba-122">public ConfigurationKeyId parentConfigurationKeyId()</span><span class="sxs-lookup"><span data-stu-id="b7fba-122">public ConfigurationKeyId parentConfigurationKeyId()</span></span>                       | <span data-ttu-id="b7fba-123">コンフィギュレーション キーの親コンフィギュレーション キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-123">Returns the ID of the parent configuration key for the configuration key.</span></span> |
| <span data-ttu-id="b7fba-124">::public static boolean enabledById(ConfigurationKeyId configurationKeyId)</span><span class="sxs-lookup"><span data-stu-id="b7fba-124">::public static boolean enabledById(ConfigurationKeyId configurationKeyId)</span></span> |                                                                           |
| <span data-ttu-id="b7fba-125">public boolean permanentlyDisabled()</span><span class="sxs-lookup"><span data-stu-id="b7fba-125">public boolean permanentlyDisabled()</span></span>                                       |                                                                           |
| <span data-ttu-id="b7fba-126">public void new(ConfigurationKeyId configurationKeyId)</span><span class="sxs-lookup"><span data-stu-id="b7fba-126">public void new(ConfigurationKeyId configurationKeyId)</span></span>                     | <span data-ttu-id="b7fba-127">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-127">Initializes a new instance of the Object class.</span></span>                           |

## <a name="method-enabled"></a><span data-ttu-id="b7fba-128">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="b7fba-128">Method enabled</span></span>

<span data-ttu-id="b7fba-129">構成キーが有効かどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-129">Returns a value that indicates whether the configuration key is enabled.</span></span>

```xpp
public boolean enabled()
```

### <a name="return-value---enabled"></a><span data-ttu-id="b7fba-130">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="b7fba-130">Return Value - enabled</span></span>

<span data-ttu-id="b7fba-131">コンフィギュレーション キーが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b7fba-131">true if the configuration key is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="b7fba-132">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="b7fba-132">Remarks - enabled</span></span>

<span data-ttu-id="b7fba-133">このメソッドを使用する例については、新しいメソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7fba-133">For an example that uses this method, see the new method.</span></span>

## <a name="method-id"></a><span data-ttu-id="b7fba-134">メソッド id</span><span class="sxs-lookup"><span data-stu-id="b7fba-134">Method id</span></span>

<span data-ttu-id="b7fba-135">コンフィギュレーション キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-135">Returns the ID of the configuration key.</span></span>

```xpp
public ConfigurationKeyId id()
```

### <a name="return-value---id"></a><span data-ttu-id="b7fba-136">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="b7fba-136">Return Value - id</span></span>

<span data-ttu-id="b7fba-137">コンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="b7fba-137">The ID of the configuration key.</span></span>

## <a name="method-label"></a><span data-ttu-id="b7fba-138">メソッド label</span><span class="sxs-lookup"><span data-stu-id="b7fba-138">Method label</span></span>

<span data-ttu-id="b7fba-139">コンフィギュレーション キーのラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-139">Returns the label for a configuration key.</span></span>

```xpp
public str label()
```

### <a name="return-value---label"></a><span data-ttu-id="b7fba-140">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="b7fba-140">Return Value - label</span></span>

<span data-ttu-id="b7fba-141">コンフィギュレーション キーのラベル。コンフィギュレーション キーにラベル値がない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="b7fba-141">The label for the configuration key; an empty string if the configuration key does not have a label value.</span></span>

## <a name="method-labelid"></a><span data-ttu-id="b7fba-142">メソッド labelId</span><span class="sxs-lookup"><span data-stu-id="b7fba-142">Method labelId</span></span>

```xpp
public str labelId()
```

### <a name="return-value---labelid"></a><span data-ttu-id="b7fba-143">戻り値 - LabelId</span><span class="sxs-lookup"><span data-stu-id="b7fba-143">Return Value - labelId</span></span>

## <a name="method-licensecode"></a><span data-ttu-id="b7fba-144">メソッド licenseCode</span><span class="sxs-lookup"><span data-stu-id="b7fba-144">Method licenseCode</span></span>

<span data-ttu-id="b7fba-145">コンフィギュレーション キーのライセンス コード ID を返します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-145">Returns the license code ID for the configuration key.</span></span>

```xpp
public LicenseCodeId licenseCode()
```

### <a name="return-value---licensecode"></a><span data-ttu-id="b7fba-146">戻り値 - licenseCode</span><span class="sxs-lookup"><span data-stu-id="b7fba-146">Return Value - licenseCode</span></span>

<span data-ttu-id="b7fba-147">コンフィギュレーション キーのライセンス コード ID。コンフィギュレーション キーにライセンス コードがない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="b7fba-147">The license code ID for the configuration key; 0 (zero) if the configuration key has no license code.</span></span>

## <a name="method-name"></a><span data-ttu-id="b7fba-148">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b7fba-148">Method name</span></span>

<span data-ttu-id="b7fba-149">コンフィギュレーション キーの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-149">Returns the name of the configuration key.</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="b7fba-150">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="b7fba-150">Return Value - name</span></span>

<span data-ttu-id="b7fba-151">コンフィギュレーション キーの名前。</span><span class="sxs-lookup"><span data-stu-id="b7fba-151">The name of the configuration key.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="b7fba-152">備考 - name</span><span class="sxs-lookup"><span data-stu-id="b7fba-152">Remarks - name</span></span>

<span data-ttu-id="b7fba-153">このメソッドを使用する例については、新しいメソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b7fba-153">For an example that uses this method, see the new method.</span></span>

## <a name="method-parentconfigurationkeyid"></a><span data-ttu-id="b7fba-154">メソッド parentConfigurationKeyId</span><span class="sxs-lookup"><span data-stu-id="b7fba-154">Method parentConfigurationKeyId</span></span>

<span data-ttu-id="b7fba-155">コンフィギュレーション キーの親コンフィギュレーション キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-155">Returns the ID of the parent configuration key for the configuration key.</span></span>

```xpp
public ConfigurationKeyId parentConfigurationKeyId()
```

### <a name="return-value---parentconfigurationkeyid"></a><span data-ttu-id="b7fba-156">戻り値 - parentConfigurationKeyId</span><span class="sxs-lookup"><span data-stu-id="b7fba-156">Return Value - parentConfigurationKeyId</span></span>

<span data-ttu-id="b7fba-157">親コンフィギュレーション キーの ID。コンフィギュレーション キーに親コンフィギュレーション キーがない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="b7fba-157">The ID of the parent configuration key; 0 (zero) if the configuration key has no parent configuration key.</span></span>

## <a name="method-enabledbyid"></a><span data-ttu-id="b7fba-158">メソッド enabledById</span><span class="sxs-lookup"><span data-stu-id="b7fba-158">Method enabledById</span></span>

```xpp
public static boolean enabledById(ConfigurationKeyId configurationKeyId)
```

### <a name="parameters---enabledbyid"></a><span data-ttu-id="b7fba-159">パラメーター - enabledById</span><span class="sxs-lookup"><span data-stu-id="b7fba-159">Parameters - enabledById</span></span>

<span data-ttu-id="b7fba-160">configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="b7fba-160">configurationKeyId</span></span>  

### <a name="return-value---enabledbyid"></a><span data-ttu-id="b7fba-161">戻り値 - enabledById</span><span class="sxs-lookup"><span data-stu-id="b7fba-161">Return Value - enabledById</span></span>

## <a name="method-permanentlydisabled"></a><span data-ttu-id="b7fba-162">メソッド permanentlyDisabled</span><span class="sxs-lookup"><span data-stu-id="b7fba-162">Method permanentlyDisabled</span></span>

```xpp
public boolean permanentlyDisabled()
```

### <a name="return-value---permanentlydisabled"></a><span data-ttu-id="b7fba-163">戻り値 - permanentlyDisabled</span><span class="sxs-lookup"><span data-stu-id="b7fba-163">Return Value - permanentlyDisabled</span></span>

## <a name="method-new"></a><span data-ttu-id="b7fba-164">メソッド new</span><span class="sxs-lookup"><span data-stu-id="b7fba-164">Method new</span></span>

<span data-ttu-id="b7fba-165">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="b7fba-165">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(ConfigurationKeyId configurationKeyId)
```

### <a name="parameters---new"></a><span data-ttu-id="b7fba-166">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="b7fba-166">Parameters - new</span></span>

<span data-ttu-id="b7fba-167">configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="b7fba-167">configurationKeyId</span></span>  
<span data-ttu-id="b7fba-168">DictConfigurationKey クラスのインスタンスを作成するために使用されるコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="b7fba-168">The ID of the configuration key that is used to create the instance of the DictConfigurationKey class.</span></span>

### <a name="examples---new"></a><span data-ttu-id="b7fba-169">例 - new</span><span class="sxs-lookup"><span data-stu-id="b7fba-169">Examples - new</span></span>

<span data-ttu-id="b7fba-170">次の例は、コンフィギュレーション キーの列挙中に DictConfigurationKey クラスの新しいインスタンスを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="b7fba-170">The following example shows how to create a new instance of the DictConfigurationKey class during an enumeration of configuration keys.</span></span>

```xpp
ConfigurationKeySet configKeySet; 
DictConfigurationKey dictConfigKey; 
str strOutput; 
int i; 
configKeySet = new ConfigurationKeySet(); 
configKeySet.loadSystemSetup(); 
// Output the configuration key names and their enable state. 
for (i=1; i <= configKeySet.cnt(); i++) 
{ 
    dictConfigKey = new DictConfigurationKey(configKeySet.cnt2Id(i)); 
    strOutput = dictConfigKey.enabled() ? "enabled" : "disabled"; 
    strOutput += " " + dictConfigKey.name(); 
    print strOutput; 
}
```

