---
title: DictEnum クラス
description: このトピックでは、DictEnum クラスについて説明します。
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
ms.openlocfilehash: aeafb4d05a4157ae5294b1543267b833a11f965f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502992"
---
# <a name="class-dictenum"></a><span data-ttu-id="3e866-103">クラス DictEnum</span><span class="sxs-lookup"><span data-stu-id="3e866-103">Class DictEnum</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictEnum extends Object
```

<span data-ttu-id="3e866-104">DictEnum クラスは、アプリケーション オブジェクト ツリー (AOT) で基本列挙の列挙値に関するメタ情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="3e866-104">The DictEnum class obtains meta-information about the base enum enumerations in the Application Object Tree (AOT).</span></span>

## <a name="remarks"></a><span data-ttu-id="3e866-105">備考</span><span class="sxs-lookup"><span data-stu-id="3e866-105">Remarks</span></span>

<span data-ttu-id="3e866-106">下位互換性については、プロパティに変換される、またはプロパティから変換されるメソッドの特別な名前付け規則が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3e866-106">For backward compatibility, a special naming convention for methods that convert to or from properties is used.</span></span>

|                 |                                |                          |
|-----------------|--------------------------------|--------------------------|
|      <span data-ttu-id="3e866-107">氏名</span><span class="sxs-lookup"><span data-stu-id="3e866-107">Name</span></span>       |            <span data-ttu-id="3e866-108">ReqDate</span><span class="sxs-lookup"><span data-stu-id="3e866-108">ReqDate</span></span>             | <span data-ttu-id="3e866-109">記号 (文字列として型設定)</span><span class="sxs-lookup"><span data-stu-id="3e866-109">Symbol (typed as string)</span></span> |
|      <span data-ttu-id="3e866-110">ラベル</span><span class="sxs-lookup"><span data-stu-id="3e866-110">Label</span></span>      | <span data-ttu-id="3e866-111">@SYS18075 (「要求日」)</span><span class="sxs-lookup"><span data-stu-id="3e866-111">@SYS18075 ("Requirement date")</span></span> |      <span data-ttu-id="3e866-112">名前またはラベル</span><span class="sxs-lookup"><span data-stu-id="3e866-112">Name or Label</span></span>       |
|   <span data-ttu-id="3e866-113">FeatureKey</span><span class="sxs-lookup"><span data-stu-id="3e866-113">FeatureKey</span></span>    |         <span data-ttu-id="3e866-114">ReqSchedAction</span><span class="sxs-lookup"><span data-stu-id="3e866-114">ReqSchedAction</span></span>         |        <span data-ttu-id="3e866-115">FeatureKey</span><span class="sxs-lookup"><span data-stu-id="3e866-115">FeatureKey</span></span>        |
|    <span data-ttu-id="3e866-116">EnumValue</span><span class="sxs-lookup"><span data-stu-id="3e866-116">EnumValue</span></span>    |               <span data-ttu-id="3e866-117">0</span><span class="sxs-lookup"><span data-stu-id="3e866-117">0</span></span>                |          <span data-ttu-id="3e866-118">先頭値</span><span class="sxs-lookup"><span data-stu-id="3e866-118">Value</span></span>           |
| <span data-ttu-id="3e866-119">AOT の位置</span><span class="sxs-lookup"><span data-stu-id="3e866-119">Position in AOT</span></span> |       <span data-ttu-id="3e866-120">最初 (インデックス = 0)</span><span class="sxs-lookup"><span data-stu-id="3e866-120">First (Index = 0)</span></span>        |          <span data-ttu-id="3e866-121">指数</span><span class="sxs-lookup"><span data-stu-id="3e866-121">Index</span></span>           |

<span data-ttu-id="3e866-122">この例では、ActionBasicDateType 基本列挙から取得されます。</span><span class="sxs-lookup"><span data-stu-id="3e866-122">This example is from the ActionBasicDateType base enum.</span></span> <span data-ttu-id="3e866-123">列挙に関する一般情報については、開発者ガイドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e866-123">For general information about enumerations, see the Developer's Guide.</span></span>

## <a name="examples"></a><span data-ttu-id="3e866-124">例</span><span class="sxs-lookup"><span data-stu-id="3e866-124">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="3e866-125">メソッド</span><span class="sxs-lookup"><span data-stu-id="3e866-125">Methods</span></span>

| <span data-ttu-id="3e866-126">方法</span><span class="sxs-lookup"><span data-stu-id="3e866-126">Method</span></span>                                                            | <span data-ttu-id="3e866-127">説明</span><span class="sxs-lookup"><span data-stu-id="3e866-127">Description</span></span>                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e866-128">public ConfigurationKeyId configurationKeyId()</span><span class="sxs-lookup"><span data-stu-id="3e866-128">public ConfigurationKeyId configurationKeyId()</span></span>                    | <span data-ttu-id="3e866-129">列挙値のコンフィギュレーション キー ID を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-129">Returns the configuration key ID for the enumeration.</span></span>                                                                     |
| <span data-ttu-id="3e866-130">public int displayLength(\[boolean useLongestLabel\])</span><span class="sxs-lookup"><span data-stu-id="3e866-130">public int displayLength(\[boolean useLongestLabel\])</span></span>             |                                                                                                                           |
| <span data-ttu-id="3e866-131">public container getCountryRegionCodes()</span><span class="sxs-lookup"><span data-stu-id="3e866-131">public container getCountryRegionCodes()</span></span>                          |                                                                                                                           |
| <span data-ttu-id="3e866-132">public str help(\[boolean useInterfaceLanguage\])</span><span class="sxs-lookup"><span data-stu-id="3e866-132">public str help(\[boolean useInterfaceLanguage\])</span></span>                 | <span data-ttu-id="3e866-133">この列挙型のヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="3e866-133">Retrieves the Help text for this enumeration.</span></span>                                                                             |
| <span data-ttu-id="3e866-134">public str helpDefined()</span><span class="sxs-lookup"><span data-stu-id="3e866-134">public str helpDefined()</span></span>                                          | <span data-ttu-id="3e866-135">この列挙型に対する help プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-135">Returns the value of the help property for this enumeration.</span></span>                                                              |
| <span data-ttu-id="3e866-136">public EnumId id()</span><span class="sxs-lookup"><span data-stu-id="3e866-136">public EnumId id()</span></span>                                                | <span data-ttu-id="3e866-137">列挙値の列挙 ID を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-137">Returns the enumeration ID of the enumeration.</span></span>                                                                            |
| <span data-ttu-id="3e866-138">public ConfigurationKeyId index2ConfigurationKey(int index)</span><span class="sxs-lookup"><span data-stu-id="3e866-138">public ConfigurationKeyId index2ConfigurationKey(int index)</span></span>       |                                                                                                                           |
| <span data-ttu-id="3e866-139">public container index2CountryRegionCodes(int index)</span><span class="sxs-lookup"><span data-stu-id="3e866-139">public container index2CountryRegionCodes(int index)</span></span>              |                                                                                                                           |
| <span data-ttu-id="3e866-140">public str index2Label(int index)</span><span class="sxs-lookup"><span data-stu-id="3e866-140">public str index2Label(int index)</span></span>                                 | <span data-ttu-id="3e866-141">インデックスにより指定される列挙項目のラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-141">Returns the label of the enumeration item that is specified by an index.</span></span>                                                  |
| <span data-ttu-id="3e866-142">public str index2LabelId(int index)</span><span class="sxs-lookup"><span data-stu-id="3e866-142">public str index2LabelId(int index)</span></span>                               |                                                                                                                           |
| <span data-ttu-id="3e866-143">public str index2Name(int index)</span><span class="sxs-lookup"><span data-stu-id="3e866-143">public str index2Name(int index)</span></span>                                  | <span data-ttu-id="3e866-144">インデックスにより指定される列挙項目のラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-144">Returns the label of the enumeration item that is specified by an index.</span></span>                                                  |
| <span data-ttu-id="3e866-145">public str index2Symbol(int index)</span><span class="sxs-lookup"><span data-stu-id="3e866-145">public str index2Symbol(int index)</span></span>                                | <span data-ttu-id="3e866-146">インデックスにより指定される列挙項目のシンボルまたは名前を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-146">Returns the symbol or name of the enumeration item that is specified by an index.</span></span>                                         |
| <span data-ttu-id="3e866-147">public int index2Value(int index)</span><span class="sxs-lookup"><span data-stu-id="3e866-147">public int index2Value(int index)</span></span>                                 | <span data-ttu-id="3e866-148">インデックスにより指定される列挙項目の値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-148">Returns the value of the enumeration item that is specified by an index.</span></span>                                                  |
| <span data-ttu-id="3e866-149">public str label()</span><span class="sxs-lookup"><span data-stu-id="3e866-149">public str label()</span></span>                                                | <span data-ttu-id="3e866-150">列挙値のラベル テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-150">Returns the label text of the enumeration.</span></span>                                                                                |
| <span data-ttu-id="3e866-151">public str labelDefined()</span><span class="sxs-lookup"><span data-stu-id="3e866-151">public str labelDefined()</span></span>                                         | <span data-ttu-id="3e866-152">この列挙型に対する label プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-152">Returns the value of the label property for this enumeration.</span></span>                                                             |
| <span data-ttu-id="3e866-153">public str name()</span><span class="sxs-lookup"><span data-stu-id="3e866-153">public str name()</span></span>                                                 | <span data-ttu-id="3e866-154">列挙型の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-154">Returns the name of the enumeration.</span></span>                                                                                      |
| <span data-ttu-id="3e866-155">public int name2Value(str name)</span><span class="sxs-lookup"><span data-stu-id="3e866-155">public int name2Value(str name)</span></span>                                   | <span data-ttu-id="3e866-156">ラベルにより参照される項目の列挙値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-156">Returns the enumeration value of the item that is referenced by its label.</span></span>                                                |
| <span data-ttu-id="3e866-157">public boolean showAsRadio()</span><span class="sxs-lookup"><span data-stu-id="3e866-157">public boolean showAsRadio()</span></span>                                      | <span data-ttu-id="3e866-158">列挙をコンボ ボックスではなくラジオ ボタンを使用して表示するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-158">Returns a value that indicates whether the enumeration should be displayed by using radio buttons instead of a combo box.</span></span> |
| <span data-ttu-id="3e866-159">public int symbol2Value(str name)</span><span class="sxs-lookup"><span data-stu-id="3e866-159">public int symbol2Value(str name)</span></span>                                 | <span data-ttu-id="3e866-160">シンボルまたは名前により参照される項目の列挙値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-160">Returns the enumeration value of the item, referenced by its symbol or name.</span></span>                                              |
| <span data-ttu-id="3e866-161">public ConfigurationKeyId value2ConfigurationKey(int value)</span><span class="sxs-lookup"><span data-stu-id="3e866-161">public ConfigurationKeyId value2ConfigurationKey(int value)</span></span>       | <span data-ttu-id="3e866-162">指定した列挙値のコンフィギュレーション キー ID を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-162">Returns the configuration key ID of a specified enumeration value.</span></span>                                                        |
| <span data-ttu-id="3e866-163">public container value2CountryRegionCodes(int value)</span><span class="sxs-lookup"><span data-stu-id="3e866-163">public container value2CountryRegionCodes(int value)</span></span>              |                                                                                                                           |
| <span data-ttu-id="3e866-164">public str value2Label(int value)</span><span class="sxs-lookup"><span data-stu-id="3e866-164">public str value2Label(int value)</span></span>                                 | <span data-ttu-id="3e866-165">指定された列挙値のラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-165">Returns the label of a specified enumeration value.</span></span>                                                                       |
| <span data-ttu-id="3e866-166">public str value2Name(int value)</span><span class="sxs-lookup"><span data-stu-id="3e866-166">public str value2Name(int value)</span></span>                                  | <span data-ttu-id="3e866-167">指定された列挙値の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-167">Returns the name of a specified enumeration value.</span></span>                                                                        |
| <span data-ttu-id="3e866-168">public str value2Symbol(int value)</span><span class="sxs-lookup"><span data-stu-id="3e866-168">public str value2Symbol(int value)</span></span>                                | <span data-ttu-id="3e866-169">記号、または指定した列挙値の Name プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-169">Returns the symbol, or the value of the Name property, of a specified enumeration value.</span></span>                                  |
| <span data-ttu-id="3e866-170">public int values()</span><span class="sxs-lookup"><span data-stu-id="3e866-170">public int values()</span></span>                                               | <span data-ttu-id="3e866-171">列挙型内の項目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-171">Returns the number of items in the enumeration.</span></span>                                                                           |
| <span data-ttu-id="3e866-172">::public static str queryFilterNames2Values(QueryFilter filter)</span><span class="sxs-lookup"><span data-stu-id="3e866-172">::public static str queryFilterNames2Values(QueryFilter filter)</span></span>   |                                                                                                                           |
| <span data-ttu-id="3e866-173">::public static str queryFilterValues2Names(QueryFilter filter)</span><span class="sxs-lookup"><span data-stu-id="3e866-173">::public static str queryFilterValues2Names(QueryFilter filter)</span></span>   |                                                                                                                           |
| <span data-ttu-id="3e866-174">::public static str queryRangeNames2Values(QueryBuildRange range)</span><span class="sxs-lookup"><span data-stu-id="3e866-174">::public static str queryRangeNames2Values(QueryBuildRange range)</span></span> |                                                                                                                           |
| <span data-ttu-id="3e866-175">::public static str queryRangeValues2Names(QueryBuildRange range)</span><span class="sxs-lookup"><span data-stu-id="3e866-175">::public static str queryRangeValues2Names(QueryBuildRange range)</span></span> |                                                                                                                           |
| <span data-ttu-id="3e866-176">::public static int value2id(AnyType value)</span><span class="sxs-lookup"><span data-stu-id="3e866-176">::public static int value2id(AnyType value)</span></span>                       | <span data-ttu-id="3e866-177">指定された値の列挙 ID を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-177">Returns the enumeration ID of a specified value.</span></span>                                                                          |
| <span data-ttu-id="3e866-178">public void new(EnumId typeId)</span><span class="sxs-lookup"><span data-stu-id="3e866-178">public void new(EnumId typeId)</span></span>                                    | <span data-ttu-id="3e866-179">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3e866-179">Initializes a new instance of the Object class.</span></span>                                                                           |

## <a name="method-configurationkeyid"></a><span data-ttu-id="3e866-180">メソッド configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="3e866-180">Method configurationKeyId</span></span>

<span data-ttu-id="3e866-181">列挙値のコンフィギュレーション キー ID を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-181">Returns the configuration key ID for the enumeration.</span></span>

```xpp
public ConfigurationKeyId configurationKeyId()
```

### <a name="return-value---configurationkeyid"></a><span data-ttu-id="3e866-182">戻り値 - configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="3e866-182">Return Value - configurationKeyId</span></span>

<span data-ttu-id="3e866-183">列挙のコンフィギュレーション キー ID がない場合の列挙のコンフィギュレーション キー ID は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="3e866-183">The configuration key ID for the enumeration; 0 (zero) if there is no configuration key ID for the enumeration.</span></span>

### <a name="examples---configurationkeyid"></a><span data-ttu-id="3e866-184">例 - configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="3e866-184">Examples - configurationKeyId</span></span>

<span data-ttu-id="3e866-185">次の例は、列挙型のコンフィギュレーション キー ID の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="3e866-185">The following example shows the retrieval of the configuration key ID for an enumeration.</span></span>

```xpp
DictEnum de; 
int      i; 
de = new DictEnum(enumName2Id("ActionType")); 
print int2str(de.configurationKeyId());
```

## <a name="method-displaylength"></a><span data-ttu-id="3e866-186">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="3e866-186">Method displayLength</span></span>

```xpp
public int displayLength([boolean useLongestLabel])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="3e866-187">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="3e866-187">Parameters - displayLength</span></span>

<span data-ttu-id="3e866-188">useLongestLabel</span><span class="sxs-lookup"><span data-stu-id="3e866-188">useLongestLabel</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="3e866-189">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="3e866-189">Return Value - displayLength</span></span>

## <a name="method-getcountryregioncodes"></a><span data-ttu-id="3e866-190">メソッド getCountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3e866-190">Method getCountryRegionCodes</span></span>

```xpp
public container getCountryRegionCodes()
```

### <a name="return-value---getcountryregioncodes"></a><span data-ttu-id="3e866-191">戻り値 - getCountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3e866-191">Return Value - getCountryRegionCodes</span></span>

## <a name="method-help"></a><span data-ttu-id="3e866-192">メソッド help</span><span class="sxs-lookup"><span data-stu-id="3e866-192">Method help</span></span>

<span data-ttu-id="3e866-193">この列挙型のヘルプ テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="3e866-193">Retrieves the Help text for this enumeration.</span></span>

```xpp
public str help([boolean useInterfaceLanguage])
```

### <a name="parameters---help"></a><span data-ttu-id="3e866-194">パラメーター - help</span><span class="sxs-lookup"><span data-stu-id="3e866-194">Parameters - help</span></span>

<span data-ttu-id="3e866-195">useInterfaceLanguage</span><span class="sxs-lookup"><span data-stu-id="3e866-195">useInterfaceLanguage</span></span>  

### <a name="return-value---help"></a><span data-ttu-id="3e866-196">戻り値 - help</span><span class="sxs-lookup"><span data-stu-id="3e866-196">Return Value - help</span></span>

<span data-ttu-id="3e866-197">ヘルプ テキストを含む文字列、ヘルプ テキストが定義されていない場合、空の文字列。</span><span class="sxs-lookup"><span data-stu-id="3e866-197">A string that contains the Help text; an empty string if no Help text is defined.</span></span>

### <a name="remarks---help"></a><span data-ttu-id="3e866-198">備考 - help</span><span class="sxs-lookup"><span data-stu-id="3e866-198">Remarks - help</span></span>

<span data-ttu-id="3e866-199">ヘルプ テキストは、基本列挙のヘルプ プロパティで定義されます。</span><span class="sxs-lookup"><span data-stu-id="3e866-199">The Help text is defined on the Help property of the base enumeration.</span></span>

## <a name="method-helpdefined"></a><span data-ttu-id="3e866-200">メソッド helpDefined</span><span class="sxs-lookup"><span data-stu-id="3e866-200">Method helpDefined</span></span>

<span data-ttu-id="3e866-201">この列挙型に対する help プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-201">Returns the value of the help property for this enumeration.</span></span>

```xpp
public str helpDefined()
```

### <a name="return-value---helpdefined"></a><span data-ttu-id="3e866-202">戻り値 - helpDefined</span><span class="sxs-lookup"><span data-stu-id="3e866-202">Return Value - helpDefined</span></span>

<span data-ttu-id="3e866-203">この列挙型に対する help プロパティの値。</span><span class="sxs-lookup"><span data-stu-id="3e866-203">The value of the help property for this enumeration.</span></span>

## <a name="method-id"></a><span data-ttu-id="3e866-204">メソッド id</span><span class="sxs-lookup"><span data-stu-id="3e866-204">Method id</span></span>

<span data-ttu-id="3e866-205">列挙値の列挙 ID を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-205">Returns the enumeration ID of the enumeration.</span></span>

```xpp
public EnumId id()
```

### <a name="return-value---id"></a><span data-ttu-id="3e866-206">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="3e866-206">Return Value - id</span></span>

<span data-ttu-id="3e866-207">この列挙の列挙 ID。</span><span class="sxs-lookup"><span data-stu-id="3e866-207">The enumeration ID of the enumeration.</span></span>

## <a name="method-index2configurationkey"></a><span data-ttu-id="3e866-208">メソッド index2ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="3e866-208">Method index2ConfigurationKey</span></span>

```xpp
public ConfigurationKeyId index2ConfigurationKey(int index)
```

### <a name="parameters---index2configurationkey"></a><span data-ttu-id="3e866-209">パラメーター - index2ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="3e866-209">Parameters - index2ConfigurationKey</span></span>

<span data-ttu-id="3e866-210">指数</span><span class="sxs-lookup"><span data-stu-id="3e866-210">index</span></span>  

### <a name="return-value---index2configurationkey"></a><span data-ttu-id="3e866-211">戻り値 - index2ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="3e866-211">Return Value - index2ConfigurationKey</span></span>

## <a name="method-index2countryregioncodes"></a><span data-ttu-id="3e866-212">メソッド index2CountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3e866-212">Method index2CountryRegionCodes</span></span>

```xpp
public container index2CountryRegionCodes(int index)
```

### <a name="parameters---index2countryregioncodes"></a><span data-ttu-id="3e866-213">パラメーター - index2CountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3e866-213">Parameters - index2CountryRegionCodes</span></span>

<span data-ttu-id="3e866-214">指数</span><span class="sxs-lookup"><span data-stu-id="3e866-214">index</span></span>  

### <a name="return-value---index2countryregioncodes"></a><span data-ttu-id="3e866-215">戻り値 - index2CountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3e866-215">Return Value - index2CountryRegionCodes</span></span>

## <a name="method-index2label"></a><span data-ttu-id="3e866-216">メソッド index2Label</span><span class="sxs-lookup"><span data-stu-id="3e866-216">Method index2Label</span></span>

<span data-ttu-id="3e866-217">インデックスにより指定される列挙項目のラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-217">Returns the label of the enumeration item that is specified by an index.</span></span>

```xpp
public str index2Label(int index)
```

### <a name="parameters---index2label"></a><span data-ttu-id="3e866-218">パラメーター - index2Label</span><span class="sxs-lookup"><span data-stu-id="3e866-218">Parameters - index2Label</span></span>

<span data-ttu-id="3e866-219">指数</span><span class="sxs-lookup"><span data-stu-id="3e866-219">index</span></span>  
<span data-ttu-id="3e866-220">AOT の列挙体の 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="3e866-220">The zero-based index of the enumeration in the AOT.</span></span>

### <a name="return-value---index2label"></a><span data-ttu-id="3e866-221">戻り値 - index2Label</span><span class="sxs-lookup"><span data-stu-id="3e866-221">Return Value - index2Label</span></span>

<span data-ttu-id="3e866-222">インデックスで指定された列挙項目のラベル。インデックスが有効な列挙項目を参照しない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="3e866-222">The label of the enumeration item that specified by index; an empty string if index does not reference a valid enumeration item.</span></span>

### <a name="examples---index2label"></a><span data-ttu-id="3e866-223">例 - index2Label</span><span class="sxs-lookup"><span data-stu-id="3e866-223">Examples - index2Label</span></span>

<span data-ttu-id="3e866-224">次の例は、列挙型内の項目のラベルの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="3e866-224">The following example shows the retrieval of the label for items in an enumeration.</span></span>

```xpp
DictEnum de; 
int      i; 
de = new DictEnum(enumName2Id("ActionType")); 
for (i=0; i < de.values(); i++) 
{ 
    print int2str(i) + ", " + de.index2Label(i); 
}
```

## <a name="method-index2labelid"></a><span data-ttu-id="3e866-225">メソッド index2LabelId</span><span class="sxs-lookup"><span data-stu-id="3e866-225">Method index2LabelId</span></span>

```xpp
public str index2LabelId(int index)
```

### <a name="parameters---index2labelid"></a><span data-ttu-id="3e866-226">パラメーター - index2LabelId</span><span class="sxs-lookup"><span data-stu-id="3e866-226">Parameters - index2LabelId</span></span>

<span data-ttu-id="3e866-227">指数</span><span class="sxs-lookup"><span data-stu-id="3e866-227">index</span></span>  

### <a name="return-value---index2labelid"></a><span data-ttu-id="3e866-228">戻り値 - index2LabelId</span><span class="sxs-lookup"><span data-stu-id="3e866-228">Return Value - index2LabelId</span></span>

## <a name="method-index2name"></a><span data-ttu-id="3e866-229">メソッド index2Name</span><span class="sxs-lookup"><span data-stu-id="3e866-229">Method index2Name</span></span>

<span data-ttu-id="3e866-230">インデックスにより指定される列挙項目のラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-230">Returns the label of the enumeration item that is specified by an index.</span></span>

```xpp
public str index2Name(int index)
```

### <a name="parameters---index2name"></a><span data-ttu-id="3e866-231">パラメーター - index2Name</span><span class="sxs-lookup"><span data-stu-id="3e866-231">Parameters - index2Name</span></span>

<span data-ttu-id="3e866-232">指数</span><span class="sxs-lookup"><span data-stu-id="3e866-232">index</span></span>  
<span data-ttu-id="3e866-233">AOT の列挙体の 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="3e866-233">The zero-based index of the enumeration in the AOT.</span></span>

### <a name="return-value---index2name"></a><span data-ttu-id="3e866-234">戻り値 - index2Name</span><span class="sxs-lookup"><span data-stu-id="3e866-234">Return Value - index2Name</span></span>

<span data-ttu-id="3e866-235">インデックスで指定された列挙項目のラベル。インデックスが有効な列挙項目を参照しない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="3e866-235">The label of the enumeration item that is specified by index; an empty string if index does not reference a valid enumeration item.</span></span>

### <a name="remarks---index2name"></a><span data-ttu-id="3e866-236">備考 - index2Name</span><span class="sxs-lookup"><span data-stu-id="3e866-236">Remarks - index2Name</span></span>

<span data-ttu-id="3e866-237">以前のバージョンとの下位互換性については、DictEnum::value2Name の「名前」は、列挙項目のラベル プロパティを参照します。</span><span class="sxs-lookup"><span data-stu-id="3e866-237">For backward compatibility with earlier versions, "Name" in DictEnum::value2Name refers to the enumeration item's label property.</span></span> <span data-ttu-id="3e866-238">コードを読みやすくするには、DictEnum::value2Name メソッドの代わりに DictEnum::value2Label メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3e866-238">To make your code more readable, use the DictEnum::value2Label method instead of the DictEnum::value2Name method.</span></span> <span data-ttu-id="3e866-239">AOT に示すように、列挙型項目の name プロパティの値を取得するには、DictEnum::value2Symbol メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3e866-239">To retrieve the value of the name property of the enumeration item as shown in the AOT, use the DictEnum::value2Symbol method.</span></span>

### <a name="examples---index2name"></a><span data-ttu-id="3e866-240">例 - index2Name</span><span class="sxs-lookup"><span data-stu-id="3e866-240">Examples - index2Name</span></span>

<span data-ttu-id="3e866-241">次の例は、列挙型内の項目のラベルの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="3e866-241">The following example shows the retrieval of the label for items in an enumeration.</span></span>

```xpp
DictEnum de; 
int      i; 
de = new DictEnum(enumName2Id("ActionType")); 
for (i=0; i < de.values(); i++) 
{ 
    print int2str(i) + ", " + de.index2Name(i); 
}
```

## <a name="method-index2symbol"></a><span data-ttu-id="3e866-242">メソッド index2Symbol</span><span class="sxs-lookup"><span data-stu-id="3e866-242">Method index2Symbol</span></span>

<span data-ttu-id="3e866-243">インデックスにより指定される列挙項目のシンボルまたは名前を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-243">Returns the symbol or name of the enumeration item that is specified by an index.</span></span>

```xpp
public str index2Symbol(int index)
```

### <a name="parameters---index2symbol"></a><span data-ttu-id="3e866-244">パラメーター - index2Symbol</span><span class="sxs-lookup"><span data-stu-id="3e866-244">Parameters - index2Symbol</span></span>

<span data-ttu-id="3e866-245">指数</span><span class="sxs-lookup"><span data-stu-id="3e866-245">index</span></span>  
<span data-ttu-id="3e866-246">AOT の列挙体の 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="3e866-246">The zero-based index of the enumeration in the AOT.</span></span>

### <a name="return-value---index2symbol"></a><span data-ttu-id="3e866-247">戻り値 - index2Symbol</span><span class="sxs-lookup"><span data-stu-id="3e866-247">Return Value - index2Symbol</span></span>

<span data-ttu-id="3e866-248">インデックスで指定される列挙型項目のシンボル。インデックスが有効な列挙型項目を参照しない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="3e866-248">The symbol of the enumeration item that is specified by index; an empty string if index does not reference a valid enumeration item.</span></span>

### <a name="remarks---index2symbol"></a><span data-ttu-id="3e866-249">備考 - index2Symbol</span><span class="sxs-lookup"><span data-stu-id="3e866-249">Remarks - index2Symbol</span></span>

<span data-ttu-id="3e866-250">シンボルは、AOT の列挙型項目の Name プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="3e866-250">The symbol corresponds to the Name property of the enumeration item in the AOT.</span></span>

### <a name="examples---index2symbol"></a><span data-ttu-id="3e866-251">例 - index2Symbol</span><span class="sxs-lookup"><span data-stu-id="3e866-251">Examples - index2Symbol</span></span>

<span data-ttu-id="3e866-252">次の例は、列挙型内の項目の記号の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="3e866-252">The following example shows the retrieval of the symbol for items in an enumeration.</span></span>

```xpp
DictEnum de; 
int      i; 
de = new DictEnum(enumName2Id("ActionType")); 
for (i=0; i < de.values(); i++) 
{ 
    print int2str(i) + ", " + de.index2Symbol(i); 
}
```

## <a name="method-index2value"></a><span data-ttu-id="3e866-253">メソッド index2Value</span><span class="sxs-lookup"><span data-stu-id="3e866-253">Method index2Value</span></span>

<span data-ttu-id="3e866-254">インデックスにより指定される列挙項目の値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-254">Returns the value of the enumeration item that is specified by an index.</span></span>

```xpp
public int index2Value(int index)
```

### <a name="parameters---index2value"></a><span data-ttu-id="3e866-255">パラメーター - index2Value</span><span class="sxs-lookup"><span data-stu-id="3e866-255">Parameters - index2Value</span></span>

<span data-ttu-id="3e866-256">指数</span><span class="sxs-lookup"><span data-stu-id="3e866-256">index</span></span>  
<span data-ttu-id="3e866-257">AOT の列挙体の 0 から始まるインデックス。</span><span class="sxs-lookup"><span data-stu-id="3e866-257">The zero-based index of the enumeration in the AOT.</span></span>

### <a name="return-value---index2value"></a><span data-ttu-id="3e866-258">戻り値 - index2Value</span><span class="sxs-lookup"><span data-stu-id="3e866-258">Return Value - index2Value</span></span>

<span data-ttu-id="3e866-259">インデックスで指定される列挙項目の値。</span><span class="sxs-lookup"><span data-stu-id="3e866-259">The value of the enumeration item that is specified by index.</span></span>

### <a name="examples---index2value"></a><span data-ttu-id="3e866-260">例 - index2Value</span><span class="sxs-lookup"><span data-stu-id="3e866-260">Examples - index2Value</span></span>

<span data-ttu-id="3e866-261">次の例は、列挙型内の項目の値の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="3e866-261">The following example shows the retrieval of the value for items in an enumeration.</span></span>

```xpp
DictEnum de; 
int      i; 
de = new DictEnum(enumName2Id("ActionType")); 
for (i=0; i < de.values(); i++) 
{ 
    print int2str(i) + ", " + int2str(de.index2Value(i)); 
}
```

## <a name="method-label"></a><span data-ttu-id="3e866-262">メソッド label</span><span class="sxs-lookup"><span data-stu-id="3e866-262">Method label</span></span>

<span data-ttu-id="3e866-263">列挙値のラベル テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-263">Returns the label text of the enumeration.</span></span>

```xpp
public str label()
```

### <a name="return-value---label"></a><span data-ttu-id="3e866-264">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="3e866-264">Return Value - label</span></span>

<span data-ttu-id="3e866-265">列挙型の名前。列挙の型ラベルがない場合は、空の文字列。</span><span class="sxs-lookup"><span data-stu-id="3e866-265">The name of the enumeration; an empty string if there is no label for the enumeration.</span></span>

## <a name="method-labeldefined"></a><span data-ttu-id="3e866-266">メソッド labelDefined</span><span class="sxs-lookup"><span data-stu-id="3e866-266">Method labelDefined</span></span>

<span data-ttu-id="3e866-267">この列挙型に対する label プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-267">Returns the value of the label property for this enumeration.</span></span>

```xpp
public str labelDefined()
```

### <a name="return-value---labeldefined"></a><span data-ttu-id="3e866-268">戻り値 - labelDefined</span><span class="sxs-lookup"><span data-stu-id="3e866-268">Return Value - labelDefined</span></span>

<span data-ttu-id="3e866-269">この列挙型に対する label プロパティの値。</span><span class="sxs-lookup"><span data-stu-id="3e866-269">The value of the label property for this enumeration.</span></span>

## <a name="method-name"></a><span data-ttu-id="3e866-270">メソッド名</span><span class="sxs-lookup"><span data-stu-id="3e866-270">Method name</span></span>

<span data-ttu-id="3e866-271">列挙型の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-271">Returns the name of the enumeration.</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="3e866-272">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="3e866-272">Return Value - name</span></span>

<span data-ttu-id="3e866-273">列挙型の名前。</span><span class="sxs-lookup"><span data-stu-id="3e866-273">The name of the enumeration.</span></span>

## <a name="method-name2value"></a><span data-ttu-id="3e866-274">メソッド name2Value</span><span class="sxs-lookup"><span data-stu-id="3e866-274">Method name2Value</span></span>

<span data-ttu-id="3e866-275">ラベルにより参照される項目の列挙値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-275">Returns the enumeration value of the item that is referenced by its label.</span></span>

```xpp
public int name2Value(str name)
```

### <a name="parameters---name2value"></a><span data-ttu-id="3e866-276">パラメーター - name2Value</span><span class="sxs-lookup"><span data-stu-id="3e866-276">Parameters - name2Value</span></span>

<span data-ttu-id="3e866-277">名前</span><span class="sxs-lookup"><span data-stu-id="3e866-277">name</span></span>  
<span data-ttu-id="3e866-278">列挙値が取得されている列挙型のラベル。</span><span class="sxs-lookup"><span data-stu-id="3e866-278">The label for the enumeration for which the enumeration value is being retrieved.</span></span>

### <a name="return-value---name2value"></a><span data-ttu-id="3e866-279">戻り値 - name2Value</span><span class="sxs-lookup"><span data-stu-id="3e866-279">Return Value - name2Value</span></span>

<span data-ttu-id="3e866-280">名前の列挙値。名前が有効な列挙ラベルでない場合は 255 です。</span><span class="sxs-lookup"><span data-stu-id="3e866-280">The enumeration value for name; 255 if name is not a valid label of an enumeration.</span></span>

### <a name="remarks---name2value"></a><span data-ttu-id="3e866-281">備考 - name2Value</span><span class="sxs-lookup"><span data-stu-id="3e866-281">Remarks - name2Value</span></span>

<span data-ttu-id="3e866-282">以前のバージョンとの下位互換性については、名前はラベルを表します。</span><span class="sxs-lookup"><span data-stu-id="3e866-282">For backward compatibility with earlier versions, name refers to the label.</span></span> <span data-ttu-id="3e866-283">ラべルの無い列挙項目は、DictEnum::name2Value メソッドを使用して見つけることができません。</span><span class="sxs-lookup"><span data-stu-id="3e866-283">Enumeration items that do not have labels cannot be found by using the DictEnum::name2Value method.</span></span>

## <a name="method-showasradio"></a><span data-ttu-id="3e866-284">メソッド showAsRadio</span><span class="sxs-lookup"><span data-stu-id="3e866-284">Method showAsRadio</span></span>

<span data-ttu-id="3e866-285">列挙をコンボ ボックスではなくラジオ ボタンを使用して表示するかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-285">Returns a value that indicates whether the enumeration should be displayed by using radio buttons instead of a combo box.</span></span>

```xpp
public boolean showAsRadio()
```

### <a name="return-value---showasradio"></a><span data-ttu-id="3e866-286">戻り値 - showAsRadio</span><span class="sxs-lookup"><span data-stu-id="3e866-286">Return Value - showAsRadio</span></span>

<span data-ttu-id="3e866-287">列挙スタイルがオプション ボタンである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="3e866-287">true if the enumeration style is radio button; otherwise, false.</span></span>

## <a name="method-symbol2value"></a><span data-ttu-id="3e866-288">メソッド symbol2Value</span><span class="sxs-lookup"><span data-stu-id="3e866-288">Method symbol2Value</span></span>

<span data-ttu-id="3e866-289">シンボルまたは名前により参照される項目の列挙値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-289">Returns the enumeration value of the item, referenced by its symbol or name.</span></span>

```xpp
public int symbol2Value(str name)
```

### <a name="parameters---symbol2value"></a><span data-ttu-id="3e866-290">パラメーター - symbol2Value</span><span class="sxs-lookup"><span data-stu-id="3e866-290">Parameters - symbol2Value</span></span>

<span data-ttu-id="3e866-291">名前</span><span class="sxs-lookup"><span data-stu-id="3e866-291">name</span></span>  
<span data-ttu-id="3e866-292">列挙値が取得されている列挙体のシンボルまたは名前。</span><span class="sxs-lookup"><span data-stu-id="3e866-292">The symbol or name for the enumeration for which the enumeration value is being retrieved.</span></span>

### <a name="return-value---symbol2value"></a><span data-ttu-id="3e866-293">戻り値 - symbol2Value</span><span class="sxs-lookup"><span data-stu-id="3e866-293">Return Value - symbol2Value</span></span>

<span data-ttu-id="3e866-294">名前の列挙値。名前が有効な列挙でない場合は 255 です。</span><span class="sxs-lookup"><span data-stu-id="3e866-294">The enumeration value for name; 255 if name is not a valid enumeration.</span></span>

## <a name="method-value2configurationkey"></a><span data-ttu-id="3e866-295">メソッド value2ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="3e866-295">Method value2ConfigurationKey</span></span>

<span data-ttu-id="3e866-296">指定した列挙値のコンフィギュレーション キー ID を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-296">Returns the configuration key ID of a specified enumeration value.</span></span>

```xpp
public ConfigurationKeyId value2ConfigurationKey(int value)
```

### <a name="parameters---value2configurationkey"></a><span data-ttu-id="3e866-297">パラメーター - value2ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="3e866-297">Parameters - value2ConfigurationKey</span></span>

<span data-ttu-id="3e866-298">値</span><span class="sxs-lookup"><span data-stu-id="3e866-298">value</span></span>  
<span data-ttu-id="3e866-299">コンフィギュレーション キーが取得されている列挙型の整数値。</span><span class="sxs-lookup"><span data-stu-id="3e866-299">The integer value for the enumeration for which the configuration key is being retrieved.</span></span>

### <a name="return-value---value2configurationkey"></a><span data-ttu-id="3e866-300">戻り値 - value2ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="3e866-300">Return Value - value2ConfigurationKey</span></span>

<span data-ttu-id="3e866-301">値のコンフィギュレーション キーがない場合または値が有効な列挙出ない場合の値のコンフィギュレーション キー ID は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="3e866-301">The configuration key ID for value; 0 (zero) if there is no configuration key for value or value is not a valid enumeration.</span></span>

## <a name="method-value2countryregioncodes"></a><span data-ttu-id="3e866-302">メソッド value2CountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3e866-302">Method value2CountryRegionCodes</span></span>

```xpp
public container value2CountryRegionCodes(int value)
```

### <a name="parameters---value2countryregioncodes"></a><span data-ttu-id="3e866-303">パラメーター - value2CountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3e866-303">Parameters - value2CountryRegionCodes</span></span>

<span data-ttu-id="3e866-304">値</span><span class="sxs-lookup"><span data-stu-id="3e866-304">value</span></span>  

### <a name="return-value---value2countryregioncodes"></a><span data-ttu-id="3e866-305">戻り値 - value2CountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="3e866-305">Return Value - value2CountryRegionCodes</span></span>

## <a name="method-value2label"></a><span data-ttu-id="3e866-306">メソッド value2Label</span><span class="sxs-lookup"><span data-stu-id="3e866-306">Method value2Label</span></span>

<span data-ttu-id="3e866-307">指定された列挙値のラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-307">Returns the label of a specified enumeration value.</span></span>

```xpp
public str value2Label(int value)
```

### <a name="parameters---value2label"></a><span data-ttu-id="3e866-308">パラメーター - value2Label</span><span class="sxs-lookup"><span data-stu-id="3e866-308">Parameters - value2Label</span></span>

<span data-ttu-id="3e866-309">値</span><span class="sxs-lookup"><span data-stu-id="3e866-309">value</span></span>  
<span data-ttu-id="3e866-310">ラベルが取得されている列挙型の整数値。</span><span class="sxs-lookup"><span data-stu-id="3e866-310">The integer value for the enumeration for which the label is being retrieved.</span></span>

### <a name="return-value---value2label"></a><span data-ttu-id="3e866-311">戻り値 - value2Label</span><span class="sxs-lookup"><span data-stu-id="3e866-311">Return Value - value2Label</span></span>

<span data-ttu-id="3e866-312">値のラベル。値または値のラベルがない場合は空の文字列は有効な列挙型ではありません。</span><span class="sxs-lookup"><span data-stu-id="3e866-312">The label for value; an empty string if there is no label for value or value is not a valid enumeration.</span></span>

### <a name="remarks---value2label"></a><span data-ttu-id="3e866-313">備考 - value2Label</span><span class="sxs-lookup"><span data-stu-id="3e866-313">Remarks - value2Label</span></span>

<span data-ttu-id="3e866-314">列挙型の品目は、ラベルを挿入する必要がありません。</span><span class="sxs-lookup"><span data-stu-id="3e866-314">Enumeration items are not required to have a label.</span></span> <span data-ttu-id="3e866-315">このメソッドを使用して、値が列挙に存在するかどうかを判断はできません。</span><span class="sxs-lookup"><span data-stu-id="3e866-315">This method cannot be used to determine whether a value exists in the enumeration.</span></span> <span data-ttu-id="3e866-316">列挙に値が存在するかどうかを確認するには、DictEnum::value2Symbol メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3e866-316">To determine whether a value exists in the enumeration, use the DictEnum::value2Symbol method.</span></span>

## <a name="method-value2name"></a><span data-ttu-id="3e866-317">メソッド value2Name</span><span class="sxs-lookup"><span data-stu-id="3e866-317">Method value2Name</span></span>

<span data-ttu-id="3e866-318">指定された列挙値の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-318">Returns the name of a specified enumeration value.</span></span>

```xpp
public str value2Name(int value)
```

### <a name="parameters---value2name"></a><span data-ttu-id="3e866-319">パラメーター - value2Name</span><span class="sxs-lookup"><span data-stu-id="3e866-319">Parameters - value2Name</span></span>

<span data-ttu-id="3e866-320">値</span><span class="sxs-lookup"><span data-stu-id="3e866-320">value</span></span>  
<span data-ttu-id="3e866-321">ラベルが取得されている列挙型の整数値。</span><span class="sxs-lookup"><span data-stu-id="3e866-321">The integer value for the enumeration for which the label is being retrieved.</span></span>

### <a name="return-value---value2name"></a><span data-ttu-id="3e866-322">戻り値 - value2Name</span><span class="sxs-lookup"><span data-stu-id="3e866-322">Return Value - value2Name</span></span>

<span data-ttu-id="3e866-323">値の名前。値または値の名前がない場合は空の文字列は有効な列挙型ではありません。</span><span class="sxs-lookup"><span data-stu-id="3e866-323">The name for value; an empty string if there is no name for value or value is not a valid enumeration.</span></span>

### <a name="remarks---value2name"></a><span data-ttu-id="3e866-324">備考 - value2Name</span><span class="sxs-lookup"><span data-stu-id="3e866-324">Remarks - value2Name</span></span>

<span data-ttu-id="3e866-325">列挙型に値が存在するかどうかを確認するには、代わりに value2Symbol メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3e866-325">To determine whether a value is in the enumeration, use the value2Symbol method instead.</span></span> <span data-ttu-id="3e866-326">列挙項目にラベルを付ける必要はないため、value2Name メソッドを使用して値が列挙型にあるかどうかを判断することはできません。</span><span class="sxs-lookup"><span data-stu-id="3e866-326">The value2Name method cannot be used to determine whether a value is in the enumeration, because enumeration items are not required to have a label.</span></span>

## <a name="method-value2symbol"></a><span data-ttu-id="3e866-327">メソッド value2Symbol</span><span class="sxs-lookup"><span data-stu-id="3e866-327">Method value2Symbol</span></span>

<span data-ttu-id="3e866-328">記号、または指定した列挙値の Name プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-328">Returns the symbol, or the value of the Name property, of a specified enumeration value.</span></span>

```xpp
public str value2Symbol(int value)
```

### <a name="parameters---value2symbol"></a><span data-ttu-id="3e866-329">パラメーター - value2Symbol</span><span class="sxs-lookup"><span data-stu-id="3e866-329">Parameters - value2Symbol</span></span>

<span data-ttu-id="3e866-330">値</span><span class="sxs-lookup"><span data-stu-id="3e866-330">value</span></span>  
<span data-ttu-id="3e866-331">記号が取得されている列挙型の整数値。</span><span class="sxs-lookup"><span data-stu-id="3e866-331">The integer value for the enumeration for which the symbol is being retrieved.</span></span>

### <a name="return-value---value2symbol"></a><span data-ttu-id="3e866-332">戻り値 - value2Symbol</span><span class="sxs-lookup"><span data-stu-id="3e866-332">Return Value - value2Symbol</span></span>

<span data-ttu-id="3e866-333">値のシンボルまたは名前。値が有効な列挙体でない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="3e866-333">The symbol or name for value; an empty string if value is not a valid enumeration.</span></span>

### <a name="remarks---value2symbol"></a><span data-ttu-id="3e866-334">備考 - value2Symbol</span><span class="sxs-lookup"><span data-stu-id="3e866-334">Remarks - value2Symbol</span></span>

<span data-ttu-id="3e866-335">列挙型の値には、記号が必要です。</span><span class="sxs-lookup"><span data-stu-id="3e866-335">Enumeration values are required to have a symbol.</span></span> <span data-ttu-id="3e866-336">このメソッドを使用すると、戻り値が空の文字列かどうかを調べることによって、列挙値が存在するかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="3e866-336">This method can be used to determine whether an enumeration value exists by checking whether the return value is an empty string.</span></span>

## <a name="method-values"></a><span data-ttu-id="3e866-337">メソッド values</span><span class="sxs-lookup"><span data-stu-id="3e866-337">Method values</span></span>

<span data-ttu-id="3e866-338">列挙型内の項目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-338">Returns the number of items in the enumeration.</span></span>

```xpp
public int values()
```

### <a name="return-value---values"></a><span data-ttu-id="3e866-339">戻り値 - values</span><span class="sxs-lookup"><span data-stu-id="3e866-339">Return Value - values</span></span>

<span data-ttu-id="3e866-340">列挙型内の項目の数。</span><span class="sxs-lookup"><span data-stu-id="3e866-340">The number of items in the enumeration.</span></span>

### <a name="remarks---values"></a><span data-ttu-id="3e866-341">備考 - values</span><span class="sxs-lookup"><span data-stu-id="3e866-341">Remarks - values</span></span>

<span data-ttu-id="3e866-342">値は一意でなければならないので、値の数は品目の数と同じです。</span><span class="sxs-lookup"><span data-stu-id="3e866-342">Because values must be unique, the number of values is the same as the number of items.</span></span>

### <a name="examples---values"></a><span data-ttu-id="3e866-343">例 - values</span><span class="sxs-lookup"><span data-stu-id="3e866-343">Examples - values</span></span>

<span data-ttu-id="3e866-344">次の例は、列挙内の項目の数を取得し、その値をループ内で使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3e866-344">The following example shows how to retrieve the number of items in an enumeration and use that value in a loop.</span></span>

```xpp
DictEnum de; 
int      i; 
de = new DictEnum(enumName2Id("ActionType")); 
for (i=0; i < de.values(); i++) 
{ 
    print int2str(i) + ", " + de.index2Name(i); 
}
```

## <a name="method-queryfilternames2values"></a><span data-ttu-id="3e866-345">メソッド queryFilterNames2Values</span><span class="sxs-lookup"><span data-stu-id="3e866-345">Method queryFilterNames2Values</span></span>

```xpp
public static str queryFilterNames2Values(QueryFilter filter)
```

### <a name="parameters---queryfilternames2values"></a><span data-ttu-id="3e866-346">パラメーター - queryFilterNames2Values</span><span class="sxs-lookup"><span data-stu-id="3e866-346">Parameters - queryFilterNames2Values</span></span>

<span data-ttu-id="3e866-347">フィルター</span><span class="sxs-lookup"><span data-stu-id="3e866-347">filter</span></span>  

### <a name="return-value---queryfilternames2values"></a><span data-ttu-id="3e866-348">戻り値 - queryFilterNames2Valuese</span><span class="sxs-lookup"><span data-stu-id="3e866-348">Return Value - queryFilterNames2Values</span></span>

## <a name="method-queryfiltervalues2names"></a><span data-ttu-id="3e866-349">メソッド queryFilterValues2Names</span><span class="sxs-lookup"><span data-stu-id="3e866-349">Method queryFilterValues2Names</span></span>

```xpp
public static str queryFilterValues2Names(QueryFilter filter)
```

### <a name="parameters---queryfiltervalues2names"></a><span data-ttu-id="3e866-350">パラメーター - queryFilterValues2Names</span><span class="sxs-lookup"><span data-stu-id="3e866-350">Parameters - queryFilterValues2Names</span></span>

<span data-ttu-id="3e866-351">フィルター</span><span class="sxs-lookup"><span data-stu-id="3e866-351">filter</span></span>  

### <a name="return-value---queryfiltervalues2names"></a><span data-ttu-id="3e866-352">戻り値 - queryFilterValues2Names</span><span class="sxs-lookup"><span data-stu-id="3e866-352">Return Value - queryFilterValues2Names</span></span>

## <a name="method-queryrangenames2values"></a><span data-ttu-id="3e866-353">メソッド queryRangeNames2Values</span><span class="sxs-lookup"><span data-stu-id="3e866-353">Method queryRangeNames2Values</span></span>

```xpp
public static str queryRangeNames2Values(QueryBuildRange range)
```

### <a name="parameters---queryrangenames2values"></a><span data-ttu-id="3e866-354">パラメーター - queryRangeNames2Values</span><span class="sxs-lookup"><span data-stu-id="3e866-354">Parameters - queryRangeNames2Values</span></span>

<span data-ttu-id="3e866-355">範囲</span><span class="sxs-lookup"><span data-stu-id="3e866-355">range</span></span>  

### <a name="return-value---queryrangenames2values"></a><span data-ttu-id="3e866-356">戻り値 - queryRangeNames2Values</span><span class="sxs-lookup"><span data-stu-id="3e866-356">Return Value - queryRangeNames2Values</span></span>

## <a name="method-queryrangevalues2names"></a><span data-ttu-id="3e866-357">メソッド queryRangeValues2Names</span><span class="sxs-lookup"><span data-stu-id="3e866-357">Method queryRangeValues2Names</span></span>

```xpp
public static str queryRangeValues2Names(QueryBuildRange range)
```

### <a name="parameters---queryrangevalues2names"></a><span data-ttu-id="3e866-358">パラメーター - queryRangeValues2Names</span><span class="sxs-lookup"><span data-stu-id="3e866-358">Parameters - queryRangeValues2Names</span></span>

<span data-ttu-id="3e866-359">範囲</span><span class="sxs-lookup"><span data-stu-id="3e866-359">range</span></span>  

### <a name="return-value---queryrangevalues2names"></a><span data-ttu-id="3e866-360">戻り値 - queryRangeValues2Names</span><span class="sxs-lookup"><span data-stu-id="3e866-360">Return Value - queryRangeValues2Names</span></span>

## <a name="method-value2id"></a><span data-ttu-id="3e866-361">メソッド value2id</span><span class="sxs-lookup"><span data-stu-id="3e866-361">Method value2id</span></span>

<span data-ttu-id="3e866-362">指定された値の列挙 ID を返します。</span><span class="sxs-lookup"><span data-stu-id="3e866-362">Returns the enumeration ID of a specified value.</span></span>

```xpp
public static int value2id(AnyType value)
```

### <a name="parameters---value2id"></a><span data-ttu-id="3e866-363">パラメーター - value2id</span><span class="sxs-lookup"><span data-stu-id="3e866-363">Parameters - value2id</span></span>

<span data-ttu-id="3e866-364">値</span><span class="sxs-lookup"><span data-stu-id="3e866-364">value</span></span>  
<span data-ttu-id="3e866-365">列挙 ID が照会されている値。</span><span class="sxs-lookup"><span data-stu-id="3e866-365">The value for which the enumeration ID is being queried.</span></span> <span data-ttu-id="3e866-366">value パラメーターは、任意のタイプを指定できます。</span><span class="sxs-lookup"><span data-stu-id="3e866-366">The value parameter can be of any type.</span></span>

### <a name="return-value---value2id"></a><span data-ttu-id="3e866-367">戻り値 - value2id</span><span class="sxs-lookup"><span data-stu-id="3e866-367">Return Value - value2id</span></span>

<span data-ttu-id="3e866-368">値が列挙の場合は値の列挙型 ID。それ以外の場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="3e866-368">The enumeration ID of value if value is an enumeration; otherwise, 0 (zero).</span></span>

### <a name="remarks---value2id"></a><span data-ttu-id="3e866-369">備考 - value2id</span><span class="sxs-lookup"><span data-stu-id="3e866-369">Remarks - value2id</span></span>

<span data-ttu-id="3e866-370">value パラメーターは、任意のタイプを指定できます。</span><span class="sxs-lookup"><span data-stu-id="3e866-370">The value parameter can be of any type.</span></span>

## <a name="method-new"></a><span data-ttu-id="3e866-371">メソッド new</span><span class="sxs-lookup"><span data-stu-id="3e866-371">Method new</span></span>

<span data-ttu-id="3e866-372">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3e866-372">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(EnumId typeId)
```

### <a name="parameters---new"></a><span data-ttu-id="3e866-373">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="3e866-373">Parameters - new</span></span>

<span data-ttu-id="3e866-374">typeId</span><span class="sxs-lookup"><span data-stu-id="3e866-374">typeId</span></span>  
<span data-ttu-id="3e866-375">列挙の ID。</span><span class="sxs-lookup"><span data-stu-id="3e866-375">The ID of the enumeration.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="3e866-376">備考 - new</span><span class="sxs-lookup"><span data-stu-id="3e866-376">Remarks - new</span></span>

<span data-ttu-id="3e866-377">無効な enum ID を指定した場合は、コンストラクターは失敗しません。</span><span class="sxs-lookup"><span data-stu-id="3e866-377">The constructor does not fail if an invalid enum ID is supplied.</span></span> <span data-ttu-id="3e866-378">ただし、DictEnum インスタンスを使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="3e866-378">However, when the DictEnum instance is used, a run-time error occurs.</span></span> <span data-ttu-id="3e866-379">EnumID 値は符号なし整数なので、常に 0 ～ 65535 の範囲であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3e866-379">Note that EnumID values are unsigned integers and are therefore always in the range 0�65535.</span></span>

### <a name="examples---new"></a><span data-ttu-id="3e866-380">例 - new</span><span class="sxs-lookup"><span data-stu-id="3e866-380">Examples - new</span></span>

<span data-ttu-id="3e866-381">次の例では、DictEnum クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="3e866-381">The following example creates an instance of the DictEnum class.</span></span>

```xpp
DictEnum de; 
de = new DictEnum(enumName2Id("ActionType"));
```

