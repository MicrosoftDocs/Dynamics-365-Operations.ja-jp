---
title: DictType クラス
description: このトピックでは、DictType クラスについて説明します。
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
ms.openlocfilehash: 36be5e4e79546ac5ba5900ddccbef6d64ecbf056
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502676"
---
# <a name="class-dicttype"></a><span data-ttu-id="7f73d-103">クラス DictType</span><span class="sxs-lookup"><span data-stu-id="7f73d-103">Class DictType</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictType extends Object
```

<span data-ttu-id="7f73d-104">DictType クラスは、拡張データ型を管理します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-104">The DictType class manages extended data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f73d-105">備考</span><span class="sxs-lookup"><span data-stu-id="7f73d-105">Remarks</span></span>

<span data-ttu-id="7f73d-106">SysDictType クラスは DictType を拡張します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-106">The SysDictType class extends DictType.</span></span>

## <a name="examples"></a><span data-ttu-id="7f73d-107">例</span><span class="sxs-lookup"><span data-stu-id="7f73d-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="7f73d-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="7f73d-108">Methods</span></span>

| <span data-ttu-id="7f73d-109">方法</span><span class="sxs-lookup"><span data-stu-id="7f73d-109">Method</span></span>                                                                | <span data-ttu-id="7f73d-110">説明</span><span class="sxs-lookup"><span data-stu-id="7f73d-110">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f73d-111">public Alignment alignment()</span><span class="sxs-lookup"><span data-stu-id="7f73d-111">public Alignment alignment()</span></span>                                          | <span data-ttu-id="7f73d-112">拡張データ型の配置を取得します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-112">Retrieves the alignment for the extended data type.</span></span>                                                                                                                      |
| <span data-ttu-id="7f73d-113">public int arraySize()</span><span class="sxs-lookup"><span data-stu-id="7f73d-113">public int arraySize()</span></span>                                                | <span data-ttu-id="7f73d-114">拡張データ型の配列サイズを提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-114">Provides the array size for an extended data type.</span></span>                                                                                                                       |
| <span data-ttu-id="7f73d-115">public Types baseType()</span><span class="sxs-lookup"><span data-stu-id="7f73d-115">public Types baseType()</span></span>                                               | <span data-ttu-id="7f73d-116">タイプ列挙値を使うことで、拡張データ型の基になるデータ型を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-116">Provides the data type on which an extended data type is based, by using the Types enumeration.</span></span>                                                                          |
| <span data-ttu-id="7f73d-117">public ConfigurationKeyId configurationKeyId()</span><span class="sxs-lookup"><span data-stu-id="7f73d-117">public ConfigurationKeyId configurationKeyId()</span></span>                        | <span data-ttu-id="7f73d-118">拡張データ型のコンフィギュレーション キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-118">Returns the ID of the configuration key for the extended data type.</span></span>                                                                                                      |
| <span data-ttu-id="7f73d-119">public int displayHeight(\[boolean useDefaults\])</span><span class="sxs-lookup"><span data-stu-id="7f73d-119">public int displayHeight(\[boolean useDefaults\])</span></span>                     | <span data-ttu-id="7f73d-120">タイプの表示の高さを取得します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-120">Retrieves the display height for the type.</span></span>                                                                                                                               |
| <span data-ttu-id="7f73d-121">public int displayLength(\[boolean useDefaults\])</span><span class="sxs-lookup"><span data-stu-id="7f73d-121">public int displayLength(\[boolean useDefaults\])</span></span>                     |                                                                                                                                                                          |
| <span data-ttu-id="7f73d-122">public EnumId enumId()</span><span class="sxs-lookup"><span data-stu-id="7f73d-122">public EnumId enumId()</span></span>                                                | <span data-ttu-id="7f73d-123">拡張データ型の基になる列挙型の ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-123">Provides the ID for the enumeration type on which an extended data type is based.</span></span>                                                                                        |
| <span data-ttu-id="7f73d-124">public ExtendedTypeId extend()</span><span class="sxs-lookup"><span data-stu-id="7f73d-124">public ExtendedTypeId extend()</span></span>                                        | <span data-ttu-id="7f73d-125">拡張データ型が拡張される拡張データ型の ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-125">Provides the ID for the extended data type that an extended data type extends.</span></span>                                                                                           |
| <span data-ttu-id="7f73d-126">public List extendedBy(\[boolean allLevels\])</span><span class="sxs-lookup"><span data-stu-id="7f73d-126">public List extendedBy(\[boolean allLevels\])</span></span>                         | <span data-ttu-id="7f73d-127">現在の EDT により拡張された拡張データ型 (EDT) のタイプ ID の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-127">Retrieves a list of type IDs for extended data types (EDTs) that are extended by the current EDT.</span></span>                                                                        |
| <span data-ttu-id="7f73d-128">public str formHelp()</span><span class="sxs-lookup"><span data-stu-id="7f73d-128">public str formHelp()</span></span>                                                 |                                                                                                                                                                          |
| <span data-ttu-id="7f73d-129">public str getControlClass()</span><span class="sxs-lookup"><span data-stu-id="7f73d-129">public str getControlClass()</span></span>                                          |                                                                                                                                                                          |
| <span data-ttu-id="7f73d-130">public container getCountryRegionCodes()</span><span class="sxs-lookup"><span data-stu-id="7f73d-130">public container getCountryRegionCodes()</span></span>                              | <span data-ttu-id="7f73d-131">定義されている国/地域コードを保持するコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-131">Retrieves a container that holds the country/region codes that are defined.</span></span>                                                                                              |
| <span data-ttu-id="7f73d-132">public DictRelation getLookupRelation(\[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="7f73d-132">public DictRelation getLookupRelation(\[int arrayIndex\])</span></span>             |                                                                                                                                                                          |
| <span data-ttu-id="7f73d-133">public AnyType getValue(\[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="7f73d-133">public AnyType getValue(\[int arrayIndex\])</span></span>                           |                                                                                                                                                                          |
| <span data-ttu-id="7f73d-134">public str help(\[int arrayIndex\], \[boolean useInterfaceLanguage\])</span><span class="sxs-lookup"><span data-stu-id="7f73d-134">public str help(\[int arrayIndex\], \[boolean useInterfaceLanguage\])</span></span> | <span data-ttu-id="7f73d-135">拡張データ型または指定した配列要素、または拡張データ型を拡張する拡張データ型に表示されるヘルプ テキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-135">Provides the Help text that is displayed for an extended data type or a specified array element, or for the extended data type that an extended data type extends.</span></span>       |
| <span data-ttu-id="7f73d-136">public str helpDefined(\[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="7f73d-136">public str helpDefined(\[int arrayIndex\])</span></span>                            | <span data-ttu-id="7f73d-137">拡張データ型の help プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-137">Returns the value of the help property for the extended data type.</span></span>                                                                                                       |
| <span data-ttu-id="7f73d-138">public ExtendedTypeId id()</span><span class="sxs-lookup"><span data-stu-id="7f73d-138">public ExtendedTypeId id()</span></span>                                            | <span data-ttu-id="7f73d-139">拡張データ型の ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-139">Provides the ID for an extended data type.</span></span>                                                                                                                               |
| <span data-ttu-id="7f73d-140">public boolean isExtendedFrom(str baseEDTName)</span><span class="sxs-lookup"><span data-stu-id="7f73d-140">public boolean isExtendedFrom(str baseEDTName)</span></span>                        | <span data-ttu-id="7f73d-141">拡張データ型が、提供される基本拡張データ型から拡張するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-141">Determines whether the extended data type extends from the base extended data type that is provided.</span></span>                                                                     |
| <span data-ttu-id="7f73d-142">public int isRadioStyle()</span><span class="sxs-lookup"><span data-stu-id="7f73d-142">public int isRadioStyle()</span></span>                                             | <span data-ttu-id="7f73d-143">列挙データ型に基づいている拡張データ型のスタイルがオプション ボタンまたはコンボ ボックスであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-143">Indicates whether the style of an extended data type that is based on an Enum data type is a radio button or a combo box.</span></span>                                                |
| <span data-ttu-id="7f73d-144">public str label(\[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="7f73d-144">public str label(\[int arrayIndex\])</span></span>                                  | <span data-ttu-id="7f73d-145">拡張データ型または指定した配列要素、または拡張データ型を拡張する拡張データ型のラベルに表示されるラベル テキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-145">Provides the label that is displayed for an extended data type or a specified array element, or the label for the extended data type that an extended data type extends.</span></span> |
| <span data-ttu-id="7f73d-146">public str labelDefined(\[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="7f73d-146">public str labelDefined(\[int arrayIndex\])</span></span>                           | <span data-ttu-id="7f73d-147">拡張データ型の label プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-147">Returns the value of the label property for the extended data type.</span></span>                                                                                                      |
| <span data-ttu-id="7f73d-148">public str lookupTable(\[boolean useInheritedMetaData\])</span><span class="sxs-lookup"><span data-stu-id="7f73d-148">public str lookupTable(\[boolean useInheritedMetaData\])</span></span>              |                                                                                                                                                                          |
| <span data-ttu-id="7f73d-149">public str name()</span><span class="sxs-lookup"><span data-stu-id="7f73d-149">public str name()</span></span>                                                     | <span data-ttu-id="7f73d-150">拡張データ型の名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-150">Provides the name of an extended data type.</span></span>                                                                                                                              |
| <span data-ttu-id="7f73d-151">public DictRelation relationObject(\[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="7f73d-151">public DictRelation relationObject(\[int arrayIndex\])</span></span>                | <span data-ttu-id="7f73d-152">DictRelation オブジェクトを返すことで、拡張データ型または指定された配列要素に対して定義されている関係に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-152">Provides information about relations that are defined for an extended data type or a specified array element by returning a DictRelation object.</span></span>                         |
| <span data-ttu-id="7f73d-153">public int stringLen()</span><span class="sxs-lookup"><span data-stu-id="7f73d-153">public int stringLen()</span></span>                                                | <span data-ttu-id="7f73d-154">文字列データ型に基づいている拡張データ型の文字列の長さを提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-154">Provides the string length for an extended data type that is based on the string data type.</span></span>                                                                              |
| <span data-ttu-id="7f73d-155">public boolean stringRight()</span><span class="sxs-lookup"><span data-stu-id="7f73d-155">public boolean stringRight()</span></span>                                          | <span data-ttu-id="7f73d-156">文字列が文字列データ型に基づいている拡張データ型で右揃えかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-156">Indicates whether the string is right-justified for an extended data type that is based on the string data type.</span></span>                                                         |
| <span data-ttu-id="7f73d-157">::public static Alignment getTypeAlignment(Types type)</span><span class="sxs-lookup"><span data-stu-id="7f73d-157">::public static Alignment getTypeAlignment(Types type)</span></span>                |                                                                                                                                                                          |
| <span data-ttu-id="7f73d-158">::public static int getTypeDisplayHeight(Types type)</span><span class="sxs-lookup"><span data-stu-id="7f73d-158">::public static int getTypeDisplayHeight(Types type)</span></span>                  |                                                                                                                                                                          |
| <span data-ttu-id="7f73d-159">::public static int getTypeDisplayLength(Types type)</span><span class="sxs-lookup"><span data-stu-id="7f73d-159">::public static int getTypeDisplayLength(Types type)</span></span>                  | <span data-ttu-id="7f73d-160">組み込み型の表示の長さを取得します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-160">Retrieves the display length for built-in types.</span></span>                                                                                                                         |
| <span data-ttu-id="7f73d-161">public void setValue(AnyType Value, \[int arrayEntry\])</span><span class="sxs-lookup"><span data-stu-id="7f73d-161">public void setValue(AnyType Value, \[int arrayEntry\])</span></span>               |                                                                                                                                                                          |
| <span data-ttu-id="7f73d-162">public void new(ExtendedTypeId typeId)</span><span class="sxs-lookup"><span data-stu-id="7f73d-162">public void new(ExtendedTypeId typeId)</span></span>                                | <span data-ttu-id="7f73d-163">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-163">Initializes a new instance of the Object class.</span></span>                                                                                                                          |
| <span data-ttu-id="7f73d-164">public void setStringLen(int stringLen)</span><span class="sxs-lookup"><span data-stu-id="7f73d-164">public void setStringLen(int stringLen)</span></span>                               | <span data-ttu-id="7f73d-165">文字列データ型に基づいている拡張データ型の文字列の長さを設定します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-165">Sets the string length for an extended data type that is based on the string data type.</span></span>                                                                                  |
| <span data-ttu-id="7f73d-166">public void setStringRight(boolean right)</span><span class="sxs-lookup"><span data-stu-id="7f73d-166">public void setStringRight(boolean right)</span></span>                             | <span data-ttu-id="7f73d-167">文字列データ型に基づいている拡張データ型の文字列の妥当性を示します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-167">Indicates the string justification for an extended data type that is based on a String data type.</span></span>                                                                        |

## <a name="method-alignment"></a><span data-ttu-id="7f73d-168">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="7f73d-168">Method alignment</span></span>

<span data-ttu-id="7f73d-169">拡張データ型の配置を取得します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-169">Retrieves the alignment for the extended data type.</span></span>

```xpp
public Alignment alignment()
```

### <a name="return-value---alignment"></a><span data-ttu-id="7f73d-170">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="7f73d-170">Return Value - alignment</span></span>

<span data-ttu-id="7f73d-171">拡張データ型の配置。</span><span class="sxs-lookup"><span data-stu-id="7f73d-171">The alignment for the extended data type.</span></span>

## <a name="method-arraysize"></a><span data-ttu-id="7f73d-172">メソッド arraySize</span><span class="sxs-lookup"><span data-stu-id="7f73d-172">Method arraySize</span></span>

<span data-ttu-id="7f73d-173">拡張データ型の配列サイズを提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-173">Provides the array size for an extended data type.</span></span>

```xpp
public int arraySize()
```

### <a name="return-value---arraysize"></a><span data-ttu-id="7f73d-174">戻り値 - arraySize</span><span class="sxs-lookup"><span data-stu-id="7f73d-174">Return Value - arraySize</span></span>

<span data-ttu-id="7f73d-175">配列サイズの整数値。拡張データ型に配列要素がない場合は 1 。</span><span class="sxs-lookup"><span data-stu-id="7f73d-175">An integer value for the array size; 1 if an extended data type does not have array elements.</span></span>

### <a name="examples---arraysize"></a><span data-ttu-id="7f73d-176">例 - arraySize</span><span class="sxs-lookup"><span data-stu-id="7f73d-176">Examples - arraySize</span></span>

<span data-ttu-id="7f73d-177">次の例では、arraySize メソッドは XMLMapDimension 拡張データ型の配列のサイズを返します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-177">In the following example, the arraySize method returns the array size for the XMLMapDimension extended data type.</span></span>

```xpp
    DictType dicttype; 
    int i; 
    dicttype = new DictType(extendedTypeNum(XMLMapDimension)); 
    for (i = 1;  i < dicttype.arraySize(); i++) 
    { 
        print dicttype.label(i); 
        pause; 
    }
```

## <a name="method-basetype"></a><span data-ttu-id="7f73d-178">メソッド baseType</span><span class="sxs-lookup"><span data-stu-id="7f73d-178">Method baseType</span></span>

<span data-ttu-id="7f73d-179">タイプ列挙値を使うことで、拡張データ型の基になるデータ型を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-179">Provides the data type on which an extended data type is based, by using the Types enumeration.</span></span>

```xpp
public Types baseType()
```

### <a name="return-value---basetype"></a><span data-ttu-id="7f73d-180">戻り値 - baseType</span><span class="sxs-lookup"><span data-stu-id="7f73d-180">Return Value - baseType</span></span>

<span data-ttu-id="7f73d-181">データ型を示すタイプ列挙値。</span><span class="sxs-lookup"><span data-stu-id="7f73d-181">A Types enumeration value that indicates the data type.</span></span>

### <a name="remarks---basetype"></a><span data-ttu-id="7f73d-182">備考 - baseType</span><span class="sxs-lookup"><span data-stu-id="7f73d-182">Remarks - baseType</span></span>

<span data-ttu-id="7f73d-183">Global::Enum2Value メソッドを使用して、戻り値を文字列に変換することができます。</span><span class="sxs-lookup"><span data-stu-id="7f73d-183">You can convert the return value to a string by using the Global::Enum2Value method.</span></span>

## <a name="method-configurationkeyid"></a><span data-ttu-id="7f73d-184">メソッド configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="7f73d-184">Method configurationKeyId</span></span>

<span data-ttu-id="7f73d-185">拡張データ型のコンフィギュレーション キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-185">Returns the ID of the configuration key for the extended data type.</span></span>

```xpp
public ConfigurationKeyId configurationKeyId()
```

### <a name="return-value---configurationkeyid"></a><span data-ttu-id="7f73d-186">戻り値 - configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="7f73d-186">Return Value - configurationKeyId</span></span>

<span data-ttu-id="7f73d-187">拡張データ型のコンフィギュレーション キーの ID。</span><span class="sxs-lookup"><span data-stu-id="7f73d-187">The ID of the configuration key for the extended data type.</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="7f73d-188">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="7f73d-188">Method displayHeight</span></span>

<span data-ttu-id="7f73d-189">タイプの表示の高さを取得します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-189">Retrieves the display height for the type.</span></span>

```xpp
public int displayHeight([boolean useDefaults])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="7f73d-190">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="7f73d-190">Parameters - displayHeight</span></span>

<span data-ttu-id="7f73d-191">useDefaults</span><span class="sxs-lookup"><span data-stu-id="7f73d-191">useDefaults</span></span>  
<span data-ttu-id="7f73d-192">タイプに長さがない場合に既定値を使用するかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="7f73d-192">A Boolean value that indicates whether to use the default values if the type does not have a length.</span></span>

### <a name="return-value---displayheight"></a><span data-ttu-id="7f73d-193">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="7f73d-193">Return Value - displayHeight</span></span>

<span data-ttu-id="7f73d-194">タイプの表示の高さ。</span><span class="sxs-lookup"><span data-stu-id="7f73d-194">The display height for the type.</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="7f73d-195">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="7f73d-195">Method displayLength</span></span>

```xpp
public int displayLength([boolean useDefaults])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="7f73d-196">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="7f73d-196">Parameters - displayLength</span></span>

<span data-ttu-id="7f73d-197">useDefaults</span><span class="sxs-lookup"><span data-stu-id="7f73d-197">useDefaults</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="7f73d-198">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="7f73d-198">Return Value - displayLength</span></span>

## <a name="method-enumid"></a><span data-ttu-id="7f73d-199">メソッド enumId</span><span class="sxs-lookup"><span data-stu-id="7f73d-199">Method enumId</span></span>

<span data-ttu-id="7f73d-200">拡張データ型の基になる列挙型の ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-200">Provides the ID for the enumeration type on which an extended data type is based.</span></span>

```xpp
public EnumId enumId()
```

### <a name="return-value---enumid"></a><span data-ttu-id="7f73d-201">戻り値 - enumId</span><span class="sxs-lookup"><span data-stu-id="7f73d-201">Return Value - enumId</span></span>

<span data-ttu-id="7f73d-202">拡張データ型の基になる列挙タイプのID。拡張データ型が列挙値に基づかない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="7f73d-202">The ID of the enumeration type on which the extended data type is based; 0 (zero) if the extended data type is not based on an enumeration.</span></span>

### <a name="remarks---enumid"></a><span data-ttu-id="7f73d-203">備考 - enumId</span><span class="sxs-lookup"><span data-stu-id="7f73d-203">Remarks - enumId</span></span>

<span data-ttu-id="7f73d-204">baseType メソッドを使用すると、拡張データ タイプのデータ タイプを判断することができます。</span><span class="sxs-lookup"><span data-stu-id="7f73d-204">You can use the baseType method to determine what the data type of an extended data type is.</span></span>

## <a name="method-extend"></a><span data-ttu-id="7f73d-205">メソッド extend</span><span class="sxs-lookup"><span data-stu-id="7f73d-205">Method extend</span></span>

<span data-ttu-id="7f73d-206">拡張データ型が拡張される拡張データ型の ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-206">Provides the ID for the extended data type that an extended data type extends.</span></span>

```xpp
public ExtendedTypeId extend()
```

### <a name="return-value---extend"></a><span data-ttu-id="7f73d-207">戻り値 - extend</span><span class="sxs-lookup"><span data-stu-id="7f73d-207">Return Value - extend</span></span>

<span data-ttu-id="7f73d-208">拡張データ型を超えた拡張データ型の ID。拡張データ型が拡張データ型を超えていない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="7f73d-208">The ID for the extended data type than an extended data type extends; 0 (zero) if the extended data type does not extend an extended data type.</span></span>

### <a name="examples---extend"></a><span data-ttu-id="7f73d-209">例 - extend</span><span class="sxs-lookup"><span data-stu-id="7f73d-209">Examples - extend</span></span>

<span data-ttu-id="7f73d-210">次の例では、拡張メソッドは ABCPercentA 拡張データ型が拡張する拡張データ型の ID を返します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-210">In the following example, the extend method returns the ID for the extended data type that the ABCPercentA extended data type extends.</span></span>

```xpp
    DictType dicttype; 
    dicttype = new DictType(extendedTypeNum(ABCPercentA)); 
    print dicttype.name() + " extends: " + extendedTypeId2Name(dicttype.extend());
```

## <a name="method-extendedby"></a><span data-ttu-id="7f73d-211">メソッド extendedBy</span><span class="sxs-lookup"><span data-stu-id="7f73d-211">Method extendedBy</span></span>

<span data-ttu-id="7f73d-212">現在の EDT により拡張された拡張データ型 (EDT) のタイプ ID の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-212">Retrieves a list of type IDs for extended data types (EDTs) that are extended by the current EDT.</span></span>

```xpp
public List extendedBy([boolean allLevels])
```

### <a name="parameters---extendedby"></a><span data-ttu-id="7f73d-213">パラメーター - extendedBy</span><span class="sxs-lookup"><span data-stu-id="7f73d-213">Parameters - extendedBy</span></span>

<span data-ttu-id="7f73d-214">allLevels</span><span class="sxs-lookup"><span data-stu-id="7f73d-214">allLevels</span></span>  

### <a name="return-value---extendedby"></a><span data-ttu-id="7f73d-215">戻り値 - extendedBy</span><span class="sxs-lookup"><span data-stu-id="7f73d-215">Return Value - extendedBy</span></span>

<span data-ttu-id="7f73d-216">現在の EDT により拡張された EDT のタイプ ID の一覧。</span><span class="sxs-lookup"><span data-stu-id="7f73d-216">A list of type IDs for EDTs that are extended by the current EDT.</span></span>

## <a name="method-formhelp"></a><span data-ttu-id="7f73d-217">メソッド formHelp</span><span class="sxs-lookup"><span data-stu-id="7f73d-217">Method formHelp</span></span>

```xpp
public str formHelp()
```

### <a name="return-value---formhelp"></a><span data-ttu-id="7f73d-218">戻り値 - formHelp</span><span class="sxs-lookup"><span data-stu-id="7f73d-218">Return Value - formHelp</span></span>

## <a name="method-getcontrolclass"></a><span data-ttu-id="7f73d-219">メソッド getControlClass</span><span class="sxs-lookup"><span data-stu-id="7f73d-219">Method getControlClass</span></span>

```xpp
public str getControlClass()
```

### <a name="return-value---getcontrolclass"></a><span data-ttu-id="7f73d-220">戻り値 - getControlClass</span><span class="sxs-lookup"><span data-stu-id="7f73d-220">Return Value - getControlClass</span></span>

## <a name="method-getcountryregioncodes"></a><span data-ttu-id="7f73d-221">メソッド getCountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="7f73d-221">Method getCountryRegionCodes</span></span>

<span data-ttu-id="7f73d-222">定義されている国/地域コードを保持するコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-222">Retrieves a container that holds the country/region codes that are defined.</span></span>

```xpp
public container getCountryRegionCodes()
```

### <a name="return-value---getcountryregioncodes"></a><span data-ttu-id="7f73d-223">戻り値 - getCountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="7f73d-223">Return Value - getCountryRegionCodes</span></span>

<span data-ttu-id="7f73d-224">国/地域コードを保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="7f73d-224">A container that holds country/region codes.</span></span>

## <a name="method-getlookuprelation"></a><span data-ttu-id="7f73d-225">メソッド getLookupRelation</span><span class="sxs-lookup"><span data-stu-id="7f73d-225">Method getLookupRelation</span></span>

```xpp
public DictRelation getLookupRelation([int arrayIndex])
```

### <a name="parameters---getlookuprelation"></a><span data-ttu-id="7f73d-226">パラメーター - getLookupRelation</span><span class="sxs-lookup"><span data-stu-id="7f73d-226">Parameters - getLookupRelation</span></span>

<span data-ttu-id="7f73d-227">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="7f73d-227">arrayIndex</span></span>  

### <a name="return-value---getlookuprelation"></a><span data-ttu-id="7f73d-228">戻り値 - getLookupRelation</span><span class="sxs-lookup"><span data-stu-id="7f73d-228">Return Value - getLookupRelation</span></span>

## <a name="method-getvalue"></a><span data-ttu-id="7f73d-229">メソッド getValue</span><span class="sxs-lookup"><span data-stu-id="7f73d-229">Method getValue</span></span>

```xpp
public AnyType getValue([int arrayIndex])
```

### <a name="parameters---getvalue"></a><span data-ttu-id="7f73d-230">パラメーター - getValue</span><span class="sxs-lookup"><span data-stu-id="7f73d-230">Parameters - getValue</span></span>

<span data-ttu-id="7f73d-231">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="7f73d-231">arrayIndex</span></span>  

### <a name="return-value---getvalue"></a><span data-ttu-id="7f73d-232">戻り値 - getValue</span><span class="sxs-lookup"><span data-stu-id="7f73d-232">Return Value - getValue</span></span>

## <a name="method-help"></a><span data-ttu-id="7f73d-233">メソッド help</span><span class="sxs-lookup"><span data-stu-id="7f73d-233">Method help</span></span>

<span data-ttu-id="7f73d-234">拡張データ型または指定した配列要素、または拡張データ型を拡張する拡張データ型に表示されるヘルプ テキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-234">Provides the Help text that is displayed for an extended data type or a specified array element, or for the extended data type that an extended data type extends.</span></span>

```xpp
public str help([int arrayIndex], [boolean useInterfaceLanguage])
```

### <a name="parameters---help"></a><span data-ttu-id="7f73d-235">パラメーター - help</span><span class="sxs-lookup"><span data-stu-id="7f73d-235">Parameters - help</span></span>

<span data-ttu-id="7f73d-236">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="7f73d-236">arrayIndex</span></span>  
<span data-ttu-id="7f73d-237">ユーザー インターフェイス言語がヘルプ テキストに使用されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="7f73d-237">A Boolean value that indicates whether the user interface language is used for the Help text; optional.</span></span>

<!-- -->

<span data-ttu-id="7f73d-238">useInterfaceLanguage</span><span class="sxs-lookup"><span data-stu-id="7f73d-238">useInterfaceLanguage</span></span>  
<span data-ttu-id="7f73d-239">ユーザー インターフェイス言語がヘルプ テキストに使用されているかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="7f73d-239">A Boolean value that indicates whether the user interface language is used for the Help text; optional.</span></span>

### <a name="return-value---help"></a><span data-ttu-id="7f73d-240">戻り値 - help</span><span class="sxs-lookup"><span data-stu-id="7f73d-240">Return Value - help</span></span>

<span data-ttu-id="7f73d-241">拡張データ型に表示されるヘルプ テキストの文字列値、または arrayEntry 値が提供される場合の配列要素。</span><span class="sxs-lookup"><span data-stu-id="7f73d-241">A string value for the Help text that is displayed for the extended data type, or for an array element if the arrayEntry value is provided.</span></span> <span data-ttu-id="7f73d-242">ヘルプ テキストは、AOT 内の拡張データ型のヘルプ テキスト プロパティ、またはアプリケーション オブジェクト ツリー (AOT) 内の配列要素に対応します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-242">The Help text corresponds to the Help Text property for an extended data type or array element in the Application Object Tree (AOT).</span></span> <span data-ttu-id="7f73d-243">拡張データ型にヘルプ テキストがないとき、このメソッドは、拡張データ型が拡張する拡張データ型に対して定義されているヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-243">When an extended data type does not have Help text, the method returns the Help text that is defined for the extended data type that the extended data type extends.</span></span>

## <a name="method-helpdefined"></a><span data-ttu-id="7f73d-244">メソッド helpDefined</span><span class="sxs-lookup"><span data-stu-id="7f73d-244">Method helpDefined</span></span>

<span data-ttu-id="7f73d-245">拡張データ型の help プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-245">Returns the value of the help property for the extended data type.</span></span>

```xpp
public str helpDefined([int arrayIndex])
```

### <a name="parameters---helpdefined"></a><span data-ttu-id="7f73d-246">パラメーター - helpDefined</span><span class="sxs-lookup"><span data-stu-id="7f73d-246">Parameters - helpDefined</span></span>

<span data-ttu-id="7f73d-247">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="7f73d-247">arrayIndex</span></span>  

### <a name="return-value---helpdefined"></a><span data-ttu-id="7f73d-248">戻り値 - helpDefined</span><span class="sxs-lookup"><span data-stu-id="7f73d-248">Return Value - helpDefined</span></span>

<span data-ttu-id="7f73d-249">拡張データ型の場合は help プロパティの値、arrayEntry 値が指定されている場合は配列要素の値。</span><span class="sxs-lookup"><span data-stu-id="7f73d-249">The value of the help property for the extended data type, or for an array element if the arrayEntry value is provided.</span></span> <span data-ttu-id="7f73d-250">ヘルプ テキストは、AOT 内の拡張データ型のヘルプ テキスト プロパティ、または AOT 内の array 要素に対応します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-250">The Help text corresponds to the Help Text property for an extended data type or array element in the AOT.</span></span>

## <a name="method-id"></a><span data-ttu-id="7f73d-251">メソッド id</span><span class="sxs-lookup"><span data-stu-id="7f73d-251">Method id</span></span>

<span data-ttu-id="7f73d-252">拡張データ型の ID を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-252">Provides the ID for an extended data type.</span></span>

```xpp
public ExtendedTypeId id()
```

### <a name="return-value---id"></a><span data-ttu-id="7f73d-253">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="7f73d-253">Return Value - id</span></span>

<span data-ttu-id="7f73d-254">拡張データ型の ID を示すデータ型の値です。</span><span class="sxs-lookup"><span data-stu-id="7f73d-254">A data type value that indicates the ID for an extended data type.</span></span>

## <a name="method-isextendedfrom"></a><span data-ttu-id="7f73d-255">メソッド isExtendedFrom</span><span class="sxs-lookup"><span data-stu-id="7f73d-255">Method isExtendedFrom</span></span>

<span data-ttu-id="7f73d-256">拡張データ型が、提供される基本拡張データ型から拡張するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-256">Determines whether the extended data type extends from the base extended data type that is provided.</span></span>

```xpp
public boolean isExtendedFrom(str baseEDTName)
```

### <a name="parameters---isextendedfrom"></a><span data-ttu-id="7f73d-257">パラメーター - isExtendedFrom</span><span class="sxs-lookup"><span data-stu-id="7f73d-257">Parameters - isExtendedFrom</span></span>

<span data-ttu-id="7f73d-258">baseEDTName</span><span class="sxs-lookup"><span data-stu-id="7f73d-258">baseEDTName</span></span>  
<span data-ttu-id="7f73d-259">拡張データ型の名前。</span><span class="sxs-lookup"><span data-stu-id="7f73d-259">The name of the extended data type.</span></span>

### <a name="return-value---isextendedfrom"></a><span data-ttu-id="7f73d-260">戻り値 - isExtendedFrom</span><span class="sxs-lookup"><span data-stu-id="7f73d-260">Return Value - isExtendedFrom</span></span>

<span data-ttu-id="7f73d-261">用意された基本拡張データ型から拡張データ型が拡張される場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7f73d-261">true if the extended data type extends from the base extended data type that is provided; otherwise, false.</span></span>

## <a name="method-isradiostyle"></a><span data-ttu-id="7f73d-262">メソッド isRadioStyle</span><span class="sxs-lookup"><span data-stu-id="7f73d-262">Method isRadioStyle</span></span>

<span data-ttu-id="7f73d-263">列挙データ型に基づいている拡張データ型のスタイルがオプション ボタンまたはコンボ ボックスであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-263">Indicates whether the style of an extended data type that is based on an Enum data type is a radio button or a combo box.</span></span>

```xpp
public int isRadioStyle()
```

### <a name="return-value---isradiostyle"></a><span data-ttu-id="7f73d-264">戻り値 - isRadioStyle</span><span class="sxs-lookup"><span data-stu-id="7f73d-264">Return Value - isRadioStyle</span></span>

<span data-ttu-id="7f73d-265">スタイルがオプション ボタンである場合は 1、それ以外の場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="7f73d-265">1 if the style is a radio button; otherwise, 0 (zero).</span></span>

## <a name="method-label"></a><span data-ttu-id="7f73d-266">メソッド label</span><span class="sxs-lookup"><span data-stu-id="7f73d-266">Method label</span></span>

<span data-ttu-id="7f73d-267">拡張データ型または指定した配列要素、または拡張データ型を拡張する拡張データ型のラベルに表示されるラベル テキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-267">Provides the label that is displayed for an extended data type or a specified array element, or the label for the extended data type that an extended data type extends.</span></span>

```xpp
public str label([int arrayIndex])
```

### <a name="parameters---label"></a><span data-ttu-id="7f73d-268">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="7f73d-268">Parameters - label</span></span>

<span data-ttu-id="7f73d-269">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="7f73d-269">arrayIndex</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="7f73d-270">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="7f73d-270">Return Value - label</span></span>

<span data-ttu-id="7f73d-271">拡張データ タイプの場合に表示されるラベル、または arrayEntry 値が指定されている場合は配列要素のラベル。</span><span class="sxs-lookup"><span data-stu-id="7f73d-271">The label that is displayed for an extended data type, or the label for an array element if the arrayEntry value is provided.</span></span> <span data-ttu-id="7f73d-272">拡張データ型にラベルがないとき、このメソッドは、拡張データ型が拡張する拡張データ型に対して定義されているラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-272">When an extended data type does not have a label, this method returns the label defined for the extended data type that an extended data type extends.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="7f73d-273">備考 - label</span><span class="sxs-lookup"><span data-stu-id="7f73d-273">Remarks - label</span></span>

<span data-ttu-id="7f73d-274">返されるラベルは、AOT の拡張データ型または配列要素のラベル プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-274">The label that is returned corresponds to the Label property for an extended data type or array element in the AOT.</span></span>

## <a name="method-labeldefined"></a><span data-ttu-id="7f73d-275">メソッド labelDefined</span><span class="sxs-lookup"><span data-stu-id="7f73d-275">Method labelDefined</span></span>

<span data-ttu-id="7f73d-276">拡張データ型の label プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-276">Returns the value of the label property for the extended data type.</span></span>

```xpp
public str labelDefined([int arrayIndex])
```

### <a name="parameters---labeldefined"></a><span data-ttu-id="7f73d-277">パラメーター - labelDefined</span><span class="sxs-lookup"><span data-stu-id="7f73d-277">Parameters - labelDefined</span></span>

<span data-ttu-id="7f73d-278">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="7f73d-278">arrayIndex</span></span>  

### <a name="return-value---labeldefined"></a><span data-ttu-id="7f73d-279">戻り値 - labelDefined</span><span class="sxs-lookup"><span data-stu-id="7f73d-279">Return Value - labelDefined</span></span>

<span data-ttu-id="7f73d-280">拡張データ型の場合は label プロパティの値、arrayEntry 値が指定されている場合は配列要素の値。</span><span class="sxs-lookup"><span data-stu-id="7f73d-280">The value of the label property for the extended data type, or for an array element if the arrayEntry value is provided.</span></span>

### <a name="remarks---labeldefined"></a><span data-ttu-id="7f73d-281">備考 - labelDefined</span><span class="sxs-lookup"><span data-stu-id="7f73d-281">Remarks - labelDefined</span></span>

<span data-ttu-id="7f73d-282">戻り値は、AOT 内の拡張データ型のラベルプロパティ、またはAOT 内の array 要素に対応します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-282">The return value corresponds to the Label property for an extended data type or array element in the AOT.</span></span>

## <a name="method-lookuptable"></a><span data-ttu-id="7f73d-283">メソッド lookupTable</span><span class="sxs-lookup"><span data-stu-id="7f73d-283">Method lookupTable</span></span>

```xpp
public str lookupTable([boolean useInheritedMetaData])
```

### <a name="parameters---lookuptable"></a><span data-ttu-id="7f73d-284">パラメーター - lookupTable</span><span class="sxs-lookup"><span data-stu-id="7f73d-284">Parameters - lookupTable</span></span>

<span data-ttu-id="7f73d-285">useInheritedMetaData</span><span class="sxs-lookup"><span data-stu-id="7f73d-285">useInheritedMetaData</span></span>  

### <a name="return-value---lookuptable"></a><span data-ttu-id="7f73d-286">戻り値 - lookupTable</span><span class="sxs-lookup"><span data-stu-id="7f73d-286">Return Value - lookupTable</span></span>

## <a name="method-name"></a><span data-ttu-id="7f73d-287">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7f73d-287">Method name</span></span>

<span data-ttu-id="7f73d-288">拡張データ型の名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-288">Provides the name of an extended data type.</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="7f73d-289">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="7f73d-289">Return Value - name</span></span>

<span data-ttu-id="7f73d-290">名前の文字列値。</span><span class="sxs-lookup"><span data-stu-id="7f73d-290">A string value for the name.</span></span> <span data-ttu-id="7f73d-291">名前は、AOT 内の拡張データ型の名前プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-291">The name corresponds to the Name property for an extended data type in the AOT.</span></span>

## <a name="method-relationobject"></a><span data-ttu-id="7f73d-292">メソッド relationObject</span><span class="sxs-lookup"><span data-stu-id="7f73d-292">Method relationObject</span></span>

<span data-ttu-id="7f73d-293">DictRelation オブジェクトを返すことで、拡張データ型または指定された配列要素に対して定義されている関係に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-293">Provides information about relations that are defined for an extended data type or a specified array element by returning a DictRelation object.</span></span>

```xpp
public DictRelation relationObject([int arrayIndex])
```

### <a name="parameters---relationobject"></a><span data-ttu-id="7f73d-294">パラメーター - relationObject</span><span class="sxs-lookup"><span data-stu-id="7f73d-294">Parameters - relationObject</span></span>

<span data-ttu-id="7f73d-295">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="7f73d-295">arrayIndex</span></span>  

### <a name="return-value---relationobject"></a><span data-ttu-id="7f73d-296">戻り値 - relationObject</span><span class="sxs-lookup"><span data-stu-id="7f73d-296">Return Value - relationObject</span></span>

<span data-ttu-id="7f73d-297">関係に関する情報を提供する DictRelation オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="7f73d-297">A DictRelation object that provides information about relations.</span></span>

### <a name="remarks---relationobject"></a><span data-ttu-id="7f73d-298">備考 - relationObject</span><span class="sxs-lookup"><span data-stu-id="7f73d-298">Remarks - relationObject</span></span>

<span data-ttu-id="7f73d-299">拡張データ型および配列要素に対して関係が定義されていない場合、DictRelation インスタンスを後続使用すると、実行時にエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-299">If no relations are defined for the extended data type and array elements, subsequent use of the DictRelation instance will cause a run-time error.</span></span>

### <a name="examples---relationobject"></a><span data-ttu-id="7f73d-300">例 - relationObject</span><span class="sxs-lookup"><span data-stu-id="7f73d-300">Examples - relationObject</span></span>

<span data-ttu-id="7f73d-301">次の例では、relationObject メソッドは XMLMapDimension 拡張データ型の DictRelation オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-301">In the following example, the relationObject method returns the DictRelation object for the XMLMapDimension extended data type.</span></span>

```xpp
    DictType dicttype; 
    DictRelation dictrelation; 
    dicttype = new DictType(extendedTypeNum(XMLMapDimension)); 
    dictrelation = dicttype.relationObject(); 
    if(dictrelation) 
    { 
        print "Relation lines: " + int2str(dictrelation.lines()); 
    } 
    else 
    { 
        print "No relations defined."; 
     }
```

## <a name="method-stringlen"></a><span data-ttu-id="7f73d-302">メソッド stringLen</span><span class="sxs-lookup"><span data-stu-id="7f73d-302">Method stringLen</span></span>

<span data-ttu-id="7f73d-303">文字列データ型に基づいている拡張データ型の文字列の長さを提供します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-303">Provides the string length for an extended data type that is based on the string data type.</span></span>

```xpp
public int stringLen()
```

### <a name="return-value---stringlen"></a><span data-ttu-id="7f73d-304">戻り値 - stringLen</span><span class="sxs-lookup"><span data-stu-id="7f73d-304">Return Value - stringLen</span></span>

<span data-ttu-id="7f73d-305">文字列の長さを示す整数。拡張データ型が文字列データ型に基づいていない場合は 0 (ゼロ) 。</span><span class="sxs-lookup"><span data-stu-id="7f73d-305">An integer that indicates the string length; 0 (zero) if an extended data type is not based on the string data type.</span></span>

## <a name="method-stringright"></a><span data-ttu-id="7f73d-306">メソッド stringRight</span><span class="sxs-lookup"><span data-stu-id="7f73d-306">Method stringRight</span></span>

<span data-ttu-id="7f73d-307">文字列が文字列データ型に基づいている拡張データ型で右揃えかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-307">Indicates whether the string is right-justified for an extended data type that is based on the string data type.</span></span>

```xpp
public boolean stringRight()
```

### <a name="return-value---stringright"></a><span data-ttu-id="7f73d-308">戻り値 - stringRight</span><span class="sxs-lookup"><span data-stu-id="7f73d-308">Return Value - stringRight</span></span>

<span data-ttu-id="7f73d-309">文字列が右揃えの場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7f73d-309">true if the string is right-justified; otherwise, false.</span></span>

### <a name="remarks---stringright"></a><span data-ttu-id="7f73d-310">備考 - stringRight</span><span class="sxs-lookup"><span data-stu-id="7f73d-310">Remarks - stringRight</span></span>

<span data-ttu-id="7f73d-311">戻り値は、AOT 内の拡張データ型の調整プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-311">The return value corresponds to the Adjustment property for the extended data type in the AOT.</span></span>

## <a name="method-gettypealignment"></a><span data-ttu-id="7f73d-312">メソッド getTypeAlignment</span><span class="sxs-lookup"><span data-stu-id="7f73d-312">Method getTypeAlignment</span></span>

```xpp
public static Alignment getTypeAlignment(Types type)
```

### <a name="parameters---gettypealignment"></a><span data-ttu-id="7f73d-313">パラメーター - getTypeAlignment</span><span class="sxs-lookup"><span data-stu-id="7f73d-313">Parameters - getTypeAlignment</span></span>

<span data-ttu-id="7f73d-314">タイプ</span><span class="sxs-lookup"><span data-stu-id="7f73d-314">type</span></span>  

### <a name="return-value---gettypealignment"></a><span data-ttu-id="7f73d-315">戻り値 - getTypeAlignment</span><span class="sxs-lookup"><span data-stu-id="7f73d-315">Return Value - getTypeAlignment</span></span>

## <a name="method-gettypedisplayheight"></a><span data-ttu-id="7f73d-316">メソッド getTypeDisplayHeight</span><span class="sxs-lookup"><span data-stu-id="7f73d-316">Method getTypeDisplayHeight</span></span>

```xpp
public static int getTypeDisplayHeight(Types type)
```

### <a name="parameters---gettypedisplayheight"></a><span data-ttu-id="7f73d-317">パラメーター - getTypeDisplayHeight</span><span class="sxs-lookup"><span data-stu-id="7f73d-317">Parameters - getTypeDisplayHeight</span></span>

<span data-ttu-id="7f73d-318">タイプ</span><span class="sxs-lookup"><span data-stu-id="7f73d-318">type</span></span>  

### <a name="return-value---gettypedisplayheight"></a><span data-ttu-id="7f73d-319">戻り値 - getTypeDisplayHeight</span><span class="sxs-lookup"><span data-stu-id="7f73d-319">Return Value - getTypeDisplayHeight</span></span>

## <a name="method-gettypedisplaylength"></a><span data-ttu-id="7f73d-320">メソッド getTypeDisplayLength</span><span class="sxs-lookup"><span data-stu-id="7f73d-320">Method getTypeDisplayLength</span></span>

<span data-ttu-id="7f73d-321">組み込み型の表示の長さを取得します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-321">Retrieves the display length for built-in types.</span></span>

```xpp
public static int getTypeDisplayLength(Types type)
```

### <a name="parameters---gettypedisplaylength"></a><span data-ttu-id="7f73d-322">パラメーター - getTypeDisplayLength</span><span class="sxs-lookup"><span data-stu-id="7f73d-322">Parameters - getTypeDisplayLength</span></span>

<span data-ttu-id="7f73d-323">タイプ</span><span class="sxs-lookup"><span data-stu-id="7f73d-323">type</span></span>  
<span data-ttu-id="7f73d-324">タイプ。</span><span class="sxs-lookup"><span data-stu-id="7f73d-324">The type.</span></span>

### <a name="return-value---gettypedisplaylength"></a><span data-ttu-id="7f73d-325">戻り値 - getTypeDisplayLength</span><span class="sxs-lookup"><span data-stu-id="7f73d-325">Return Value - getTypeDisplayLength</span></span>

<span data-ttu-id="7f73d-326">組み込み型の表示の長さ。</span><span class="sxs-lookup"><span data-stu-id="7f73d-326">The display length for the built-in type.</span></span>

## <a name="method-setvalue"></a><span data-ttu-id="7f73d-327">メソッド setValue</span><span class="sxs-lookup"><span data-stu-id="7f73d-327">Method setValue</span></span>

```xpp
public void setValue(AnyType Value, [int arrayEntry])
```

### <a name="parameters---setvalue"></a><span data-ttu-id="7f73d-328">パラメーター - setValue</span><span class="sxs-lookup"><span data-stu-id="7f73d-328">Parameters - setValue</span></span>

<span data-ttu-id="7f73d-329">先頭値</span><span class="sxs-lookup"><span data-stu-id="7f73d-329">Value</span></span>  

<!-- -->

<span data-ttu-id="7f73d-330">arrayEntry</span><span class="sxs-lookup"><span data-stu-id="7f73d-330">arrayEntry</span></span>  

## <a name="method-new"></a><span data-ttu-id="7f73d-331">メソッド new</span><span class="sxs-lookup"><span data-stu-id="7f73d-331">Method new</span></span>

<span data-ttu-id="7f73d-332">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-332">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(ExtendedTypeId typeId)
```

### <a name="parameters---new"></a><span data-ttu-id="7f73d-333">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="7f73d-333">Parameters - new</span></span>

<span data-ttu-id="7f73d-334">typeId</span><span class="sxs-lookup"><span data-stu-id="7f73d-334">typeId</span></span>  
<span data-ttu-id="7f73d-335">拡張データ型の ID を示すデータ型です。</span><span class="sxs-lookup"><span data-stu-id="7f73d-335">A data type that indicates the ID for an extended data type.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="7f73d-336">備考 - new</span><span class="sxs-lookup"><span data-stu-id="7f73d-336">Remarks - new</span></span>

<span data-ttu-id="7f73d-337">TypeId 値が無効な拡張データ型 ID である場合にこのコンストラクターは失敗しません。ただし、DictType インスタンスを使用すると、実行時にエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-337">This constructor does not fail if the typeId value is an invalid extended data type ID; however, when the DictType instance is used, a run-time error occurs.</span></span> <span data-ttu-id="7f73d-338">extendedTypeNum 関数を使用して、ID の代わりに拡張データ タイプの名前を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="7f73d-338">You can pass the name of the extended data type instead of an ID by using the extendedTypeNum function.</span></span>

### <a name="examples---new"></a><span data-ttu-id="7f73d-339">例 - new</span><span class="sxs-lookup"><span data-stu-id="7f73d-339">Examples - new</span></span>

<span data-ttu-id="7f73d-340">次の例は、DictType クラスのインスタンスを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7f73d-340">The following example shows how to create an instance of the DictType class.</span></span>

```xpp
    DictType dicttype; 
    dicttype = new DictType(extendedTypeNum(ABCModelType));
```

## <a name="method-setstringlen"></a><span data-ttu-id="7f73d-341">メソッド setStringLen</span><span class="sxs-lookup"><span data-stu-id="7f73d-341">Method setStringLen</span></span>

<span data-ttu-id="7f73d-342">文字列データ型に基づいている拡張データ型の文字列の長さを設定します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-342">Sets the string length for an extended data type that is based on the string data type.</span></span>

```xpp
public void setStringLen(int stringLen)
```

### <a name="parameters---setstringlen"></a><span data-ttu-id="7f73d-343">パラメーター - setStringLen</span><span class="sxs-lookup"><span data-stu-id="7f73d-343">Parameters - setStringLen</span></span>

<span data-ttu-id="7f73d-344">stringLen</span><span class="sxs-lookup"><span data-stu-id="7f73d-344">stringLen</span></span>  
<span data-ttu-id="7f73d-345">文字列の長さを示す整数。</span><span class="sxs-lookup"><span data-stu-id="7f73d-345">An integer that indicates the string length.</span></span>

### <a name="remarks---setstringlen"></a><span data-ttu-id="7f73d-346">備考 - setStringLen</span><span class="sxs-lookup"><span data-stu-id="7f73d-346">Remarks - setStringLen</span></span>

<span data-ttu-id="7f73d-347">このメソッドを使用すると、X++ コードとメタデータを作成、読み込み、更新、および削除ができます。</span><span class="sxs-lookup"><span data-stu-id="7f73d-347">This method lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="7f73d-348">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-348">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span> <span data-ttu-id="7f73d-349">文字列の長さは、AOT 内の拡張データ型 StringSize プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-349">The string length corresponds to the StringSize property for the extended data type in the AOT.</span></span>

### <a name="examples---setstringlen"></a><span data-ttu-id="7f73d-350">例 - setStringLen</span><span class="sxs-lookup"><span data-stu-id="7f73d-350">Examples - setStringLen</span></span>

<span data-ttu-id="7f73d-351">次の例では、AccountName 拡張データ型の StringSize プロパティを 10 に設定します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-351">The following example sets the StringSize property to 10 for the AccountName extended data type.</span></span>

```xpp
server static public void Main(Args _args) 
{ 
    DictType  dt; 
    dt = new DictType(ExtendedTypeNum(AccountName)); 
    if (dt) 
    { 
        dt.setStringLen(10); 
    } 
}
```

## <a name="method-setstringright"></a><span data-ttu-id="7f73d-352">メソッド setStringRight</span><span class="sxs-lookup"><span data-stu-id="7f73d-352">Method setStringRight</span></span>

<span data-ttu-id="7f73d-353">文字列データ型に基づいている拡張データ型の文字列の妥当性を示します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-353">Indicates the string justification for an extended data type that is based on a String data type.</span></span>

```xpp
public void setStringRight(boolean right)
```

### <a name="parameters---setstringright"></a><span data-ttu-id="7f73d-354">パラメーター - setStringRight</span><span class="sxs-lookup"><span data-stu-id="7f73d-354">Parameters - setStringRight</span></span>

<span data-ttu-id="7f73d-355">権限</span><span class="sxs-lookup"><span data-stu-id="7f73d-355">right</span></span>  
<span data-ttu-id="7f73d-356">ブール値: 右揃え文字列の場合は true、左揃え文字列の場合は false。</span><span class="sxs-lookup"><span data-stu-id="7f73d-356">A Boolean value: true for a right-justified string and false for a left-justified string.</span></span>

### <a name="remarks---setstringright"></a><span data-ttu-id="7f73d-357">備考 - setStringRight</span><span class="sxs-lookup"><span data-stu-id="7f73d-357">Remarks - setStringRight</span></span>

<span data-ttu-id="7f73d-358">このメソッドを使用すると、X++ コードとメタデータを作成、読み込み、更新、および削除ができます。</span><span class="sxs-lookup"><span data-stu-id="7f73d-358">This method lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="7f73d-359">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-359">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples---setstringright"></a><span data-ttu-id="7f73d-360">例 - setStringRight</span><span class="sxs-lookup"><span data-stu-id="7f73d-360">Examples - setStringRight</span></span>

<span data-ttu-id="7f73d-361">次の例では、AccountName 拡張データ型の正当性を設定します。</span><span class="sxs-lookup"><span data-stu-id="7f73d-361">The following example sets the justification of the AccountName extended data type.</span></span>

```xpp
server static public void Main(Args _args) 
{ 
    DictType dt; 
    dt = new DictType(ExtendedTypeNum(AccountName)); 
    if (dt) 
    { 
        dt.setStringRight(true); 
    } 
}
```

