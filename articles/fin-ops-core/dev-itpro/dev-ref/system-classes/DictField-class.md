---
title: DictField クラス
description: このトピックでは、DictField クラスについて説明します。
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
ms.openlocfilehash: 97ec4e1feb50e2d92355f3e6331b0b315d2968b6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502990"
---
# <a name="class-dictfield"></a><span data-ttu-id="44ed7-103">クラス DictField</span><span class="sxs-lookup"><span data-stu-id="44ed7-103">Class DictField</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DictField extends Object
```

<span data-ttu-id="44ed7-104">DictField クラスは、指定されたテーブルで指定したフィールドに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-104">The DictField class provides information about a specified field in a specified table.</span></span>

## <a name="remarks"></a><span data-ttu-id="44ed7-105">備考</span><span class="sxs-lookup"><span data-stu-id="44ed7-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="44ed7-106">例</span><span class="sxs-lookup"><span data-stu-id="44ed7-106">Examples</span></span>

<span data-ttu-id="44ed7-107">次の例は、フィールドが必須かどうかを判断するために DictField クラスのインスタンスを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-107">The following example shows how to create an instance of the DictField class to determine whether a field is mandatory.</span></span>

```xpp
macrolib.dictfield 
DictField df; 
int       nFlags; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    nFlags = df.flags(); 
    if (bitTest(nFlags,#DBF_MANDATORY)) 
    { 
        print ("The field is mandatory."); 
    } 
    else 
    { 
        print ("The field is not mandatory."); 
    } 
}
```

## <a name="methods"></a><span data-ttu-id="44ed7-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="44ed7-108">Methods</span></span>

| <span data-ttu-id="44ed7-109">方法</span><span class="sxs-lookup"><span data-stu-id="44ed7-109">Method</span></span>                                                                                                                | <span data-ttu-id="44ed7-110">説明</span><span class="sxs-lookup"><span data-stu-id="44ed7-110">Description</span></span>                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44ed7-111">public FieldId aliasFor()</span><span class="sxs-lookup"><span data-stu-id="44ed7-111">public FieldId aliasFor()</span></span>                                                                                             | <span data-ttu-id="44ed7-112">フィールドが別のフィールドのエイリアスの場合は、エイリアス フィールドの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-112">Returns the ID of the alias field, if the field is an alias for another field.</span></span>                                                            |
| <span data-ttu-id="44ed7-113">public Alignment alignment()</span><span class="sxs-lookup"><span data-stu-id="44ed7-113">public Alignment alignment()</span></span>                                                                                          |                                                                                                                                           |
| <span data-ttu-id="44ed7-114">public boolean allowEdit()</span><span class="sxs-lookup"><span data-stu-id="44ed7-114">public boolean allowEdit()</span></span>                                                                                            |                                                                                                                                           |
| <span data-ttu-id="44ed7-115">public boolean allowEditOnCreate()</span><span class="sxs-lookup"><span data-stu-id="44ed7-115">public boolean allowEditOnCreate()</span></span>                                                                                    |                                                                                                                                           |
| <span data-ttu-id="44ed7-116">public boolean aosAuthorization()</span><span class="sxs-lookup"><span data-stu-id="44ed7-116">public boolean aosAuthorization()</span></span>                                                                                     |                                                                                                                                           |
| <span data-ttu-id="44ed7-117">public int arrayIndex()</span><span class="sxs-lookup"><span data-stu-id="44ed7-117">public int arrayIndex()</span></span>                                                                                               |                                                                                                                                           |
| <span data-ttu-id="44ed7-118">public int arraySize()</span><span class="sxs-lookup"><span data-stu-id="44ed7-118">public int arraySize()</span></span>                                                                                                | <span data-ttu-id="44ed7-119">フィールドの配列サイズを返します (つまり、基になる拡張データ型の配列サイズ)。</span><span class="sxs-lookup"><span data-stu-id="44ed7-119">Returns the array size for the field (in other words, the array size of the underlying extended data type).</span></span>                               |
| <span data-ttu-id="44ed7-120">public Types baseType()</span><span class="sxs-lookup"><span data-stu-id="44ed7-120">public Types baseType()</span></span>                                                                                               | <span data-ttu-id="44ed7-121">文字列、実数、整数、日付、時刻、列挙、またはコンテナーなど、フィールドの基本型を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-121">Returns the base type of the field, such as string, real, integer, date, time, enum, or container.</span></span>                                        |
| <span data-ttu-id="44ed7-122">public ConfigurationKeyId configurationKeyId()</span><span class="sxs-lookup"><span data-stu-id="44ed7-122">public ConfigurationKeyId configurationKeyId()</span></span>                                                                        | <span data-ttu-id="44ed7-123">フィールドのコンフィギュレーション キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-123">Returns the ID of the configuration key for the field.</span></span>                                                                                    |
| <span data-ttu-id="44ed7-124">public str dateTimeTimeZoneRuleFieldName(\[int arrayindex\])</span><span class="sxs-lookup"><span data-stu-id="44ed7-124">public str dateTimeTimeZoneRuleFieldName(\[int arrayindex\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="44ed7-125">public int displayHeight(\[boolean useDefaults\])</span><span class="sxs-lookup"><span data-stu-id="44ed7-125">public int displayHeight(\[boolean useDefaults\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="44ed7-126">public int displayLength(\[boolean useDefaults\])</span><span class="sxs-lookup"><span data-stu-id="44ed7-126">public int displayLength(\[boolean useDefaults\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="44ed7-127">public EnumId enumId()</span><span class="sxs-lookup"><span data-stu-id="44ed7-127">public EnumId enumId()</span></span>                                                                                                | <span data-ttu-id="44ed7-128">フィールドが列挙型に基づいている場合は列挙型の ID を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-128">Returns the ID of the enumeration if the field is based on an enumeration.</span></span>                                                                |
| <span data-ttu-id="44ed7-129">public int flags(\[str ext\], \[Common record\])</span><span class="sxs-lookup"><span data-stu-id="44ed7-129">public int flags(\[str ext\], \[Common record\])</span></span>                                                                      | <span data-ttu-id="44ed7-130">フィールドのプロパティを定義する整数を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-130">Returns an integer that defines the properties of the field.</span></span> <span data-ttu-id="44ed7-131">DBF\_MANDATORY、などのフラグ値は、DictField マクロで定義されています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-131">The flag values, such as DBF\_MANDATORY, are defined in the DictField macro.</span></span> |
| <span data-ttu-id="44ed7-132">public container getCountryRegionCodes()</span><span class="sxs-lookup"><span data-stu-id="44ed7-132">public container getCountryRegionCodes()</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="44ed7-133">public FieldId getCountryRegionContextField()</span><span class="sxs-lookup"><span data-stu-id="44ed7-133">public FieldId getCountryRegionContextField()</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="44ed7-134">public str getPrimaryTableForSurrogateField()</span><span class="sxs-lookup"><span data-stu-id="44ed7-134">public str getPrimaryTableForSurrogateField()</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="44ed7-135">public str groupPrompt()</span><span class="sxs-lookup"><span data-stu-id="44ed7-135">public str groupPrompt()</span></span>                                                                                              | <span data-ttu-id="44ed7-136">フィールドの groupPrompt 値を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-136">Returns the groupPrompt value for the field.</span></span>                                                                                              |
| <span data-ttu-id="44ed7-137">public str groupPromptDefined()</span><span class="sxs-lookup"><span data-stu-id="44ed7-137">public str groupPromptDefined()</span></span>                                                                                       | <span data-ttu-id="44ed7-138">フィールドの groupPrompt プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-138">Returns the value of the groupPrompt property for the field.</span></span>                                                                              |
| <span data-ttu-id="44ed7-139">public str help(\[int arrayIndex\], \[boolean useInterfaceLanguage\])</span><span class="sxs-lookup"><span data-stu-id="44ed7-139">public str help(\[int arrayIndex\], \[boolean useInterfaceLanguage\])</span></span>                                                 | <span data-ttu-id="44ed7-140">フィールドについて表示されるヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-140">Returns the Help text that is displayed for the field.</span></span>                                                                                    |
| <span data-ttu-id="44ed7-141">public str helpDefined()</span><span class="sxs-lookup"><span data-stu-id="44ed7-141">public str helpDefined()</span></span>                                                                                              | <span data-ttu-id="44ed7-142">フィールドの help プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-142">Returns the value of the help property for the field.</span></span>                                                                                     |
| <span data-ttu-id="44ed7-143">public FieldId id()</span><span class="sxs-lookup"><span data-stu-id="44ed7-143">public FieldId id()</span></span>                                                                                                   | <span data-ttu-id="44ed7-144">フィールドの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-144">Returns the ID of the field.</span></span>                                                                                                              |
| <span data-ttu-id="44ed7-145">public boolean isIgnoreEDTRelation()</span><span class="sxs-lookup"><span data-stu-id="44ed7-145">public boolean isIgnoreEDTRelation()</span></span>                                                                                  |                                                                                                                                           |
| <span data-ttu-id="44ed7-146">public boolean isMonocased()</span><span class="sxs-lookup"><span data-stu-id="44ed7-146">public boolean isMonocased()</span></span>                                                                                          | <span data-ttu-id="44ed7-147">フィールドが monocase であるデータベースが必要とするかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-147">Returns a value that indicates whether the database requires that the field be monocase.</span></span>                                                  |
| <span data-ttu-id="44ed7-148">public boolean isSql()</span><span class="sxs-lookup"><span data-stu-id="44ed7-148">public boolean isSql()</span></span>                                                                                                | <span data-ttu-id="44ed7-149">フィールドが SQL データベースにあるかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-149">Returns a value that indicates whether the field is in the SQL database.</span></span>                                                                  |
| <span data-ttu-id="44ed7-150">public boolean isSurrogateForeignKey()</span><span class="sxs-lookup"><span data-stu-id="44ed7-150">public boolean isSurrogateForeignKey()</span></span>                                                                                |                                                                                                                                           |
| <span data-ttu-id="44ed7-151">public boolean isSystem()</span><span class="sxs-lookup"><span data-stu-id="44ed7-151">public boolean isSystem()</span></span>                                                                                             | <span data-ttu-id="44ed7-152">フィールドがシステム フィールドかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-152">Returns a value that indicates whether the field is a system field.</span></span>                                                                       |
| <span data-ttu-id="44ed7-153">public str label(\[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="44ed7-153">public str label(\[int arrayIndex\])</span></span>                                                                                  | <span data-ttu-id="44ed7-154">フィールドのラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-154">Returns the label for the field.</span></span>                                                                                                          |
| <span data-ttu-id="44ed7-155">public str labelDefined()</span><span class="sxs-lookup"><span data-stu-id="44ed7-155">public str labelDefined()</span></span>                                                                                             | <span data-ttu-id="44ed7-156">フィールドの label プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-156">Returns the value of the label property for the field.</span></span>                                                                                    |
| <span data-ttu-id="44ed7-157">public boolean mandatory()</span><span class="sxs-lookup"><span data-stu-id="44ed7-157">public boolean mandatory()</span></span>                                                                                            |                                                                                                                                           |
| <span data-ttu-id="44ed7-158">public str name(\[DbBackend db\], \[int arrayindex\], \[FieldNameGenerationMode generationMode\], \[str tableAlias\])</span><span class="sxs-lookup"><span data-stu-id="44ed7-158">public str name(\[DbBackend db\], \[int arrayindex\], \[FieldNameGenerationMode generationMode\], \[str tableAlias\])</span></span> | <span data-ttu-id="44ed7-159">フィールドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-159">Returns the name of the field.</span></span>                                                                                                            |
| <span data-ttu-id="44ed7-160">public Guid origin()</span><span class="sxs-lookup"><span data-stu-id="44ed7-160">public Guid origin()</span></span>                                                                                                  |                                                                                                                                           |
| <span data-ttu-id="44ed7-161">public str qualifiedLabel(\[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="44ed7-161">public str qualifiedLabel(\[int arrayIndex\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="44ed7-162">public str relatedTableName()</span><span class="sxs-lookup"><span data-stu-id="44ed7-162">public str relatedTableName()</span></span>                                                                                         |                                                                                                                                           |
| <span data-ttu-id="44ed7-163">public str relationContext()</span><span class="sxs-lookup"><span data-stu-id="44ed7-163">public str relationContext()</span></span>                                                                                          |                                                                                                                                           |
| <span data-ttu-id="44ed7-164">public DictRelation relationObject(\[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="44ed7-164">public DictRelation relationObject(\[int arrayIndex\])</span></span>                                                                | <span data-ttu-id="44ed7-165">フィールドが関係のある拡張データ型に基づいている場合、フィールドの DictRelation オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-165">Returns a DictRelation object for the field if the field is based on an extended data type that has a relation.</span></span>                           |
| <span data-ttu-id="44ed7-166">public AccessType rights(\[boolean ignoreContext\])</span><span class="sxs-lookup"><span data-stu-id="44ed7-166">public AccessType rights(\[boolean ignoreContext\])</span></span>                                                                   | <span data-ttu-id="44ed7-167">このフィールドに指定されている、現在のユーザーのアクセス権を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-167">Returns the access rights for the current user that are specified for the field.</span></span>                                                          |
| <span data-ttu-id="44ed7-168">public int stringLen()</span><span class="sxs-lookup"><span data-stu-id="44ed7-168">public int stringLen()</span></span>                                                                                                | <span data-ttu-id="44ed7-169">フィールドの基本型が文字列の場合、フィールドの文字列サイズを返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-169">Returns the string size of the field if the base type of the field is a string.</span></span>                                                           |
| <span data-ttu-id="44ed7-170">public TableId tableid()</span><span class="sxs-lookup"><span data-stu-id="44ed7-170">public TableId tableid()</span></span>                                                                                              | <span data-ttu-id="44ed7-171">フィールドを含むテーブルの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-171">Returns the ID of the table that contains the field.</span></span>                                                                                      |
| <span data-ttu-id="44ed7-172">public Types type()</span><span class="sxs-lookup"><span data-stu-id="44ed7-172">public Types type()</span></span>                                                                                                   | <span data-ttu-id="44ed7-173">フィールドのデータ型を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-173">Returns the data type of the field.</span></span>                                                                                                       |
| <span data-ttu-id="44ed7-174">public ExtendedTypeId typeId()</span><span class="sxs-lookup"><span data-stu-id="44ed7-174">public ExtendedTypeId typeId()</span></span>                                                                                        | <span data-ttu-id="44ed7-175">このフィールドが拡張データ型に基づいている場合は、拡張データ型の ID を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-175">Returns the ID of the extended data type if the field is based on an extended data type.</span></span>                                                  |
| <span data-ttu-id="44ed7-176">public boolean visible()</span><span class="sxs-lookup"><span data-stu-id="44ed7-176">public boolean visible()</span></span>                                                                                              |                                                                                                                                           |
| <span data-ttu-id="44ed7-177">public void setLookupMode(boolean lookupMode)</span><span class="sxs-lookup"><span data-stu-id="44ed7-177">public void setLookupMode(boolean lookupMode)</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="44ed7-178">public void setSFKAutoAuthorizationMode(boolean sfkMode)</span><span class="sxs-lookup"><span data-stu-id="44ed7-178">public void setSFKAutoAuthorizationMode(boolean sfkMode)</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="44ed7-179">public void new(TableId tableId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="44ed7-179">public void new(TableId tableId, FieldId fieldId, \[int arrayIndex\])</span></span>                                                 | <span data-ttu-id="44ed7-180">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-180">Initializes a new instance of the Object class.</span></span>                                                                                           |

## <a name="method-aliasfor"></a><span data-ttu-id="44ed7-181">メソッド aliasFor</span><span class="sxs-lookup"><span data-stu-id="44ed7-181">Method aliasFor</span></span>

<span data-ttu-id="44ed7-182">フィールドが別のフィールドのエイリアスの場合は、エイリアス フィールドの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-182">Returns the ID of the alias field, if the field is an alias for another field.</span></span>

```xpp
public FieldId aliasFor()
```

### <a name="return-value---aliasfor"></a><span data-ttu-id="44ed7-183">戻り値 - aliasFor</span><span class="sxs-lookup"><span data-stu-id="44ed7-183">Return Value - aliasFor</span></span>

<span data-ttu-id="44ed7-184">フィールドのエイリアス フィールドの ID。フィールドが別のフィールドのエイリアスでない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="44ed7-184">The ID of the alias field for the field; 0 (zero) if the field is not an alias for another field.</span></span>

### <a name="remarks---aliasfor"></a><span data-ttu-id="44ed7-185">備考 - aliasFor</span><span class="sxs-lookup"><span data-stu-id="44ed7-185">Remarks - aliasFor</span></span>

<span data-ttu-id="44ed7-186">ユーザーがデータをフィールドに入力すると、そのテーブルの validateField メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="44ed7-186">When the user enters data in a field, the validateField method of the table is called.</span></span> <span data-ttu-id="44ed7-187">validateField メソッドが値に対する参照を実行することができない場合、エイリアスが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-187">If the validateField method cannot perform a lookup on the value, it checks whether an alias exists.</span></span> <span data-ttu-id="44ed7-188">エイリアス フィールドが存在する場合、validateField メソッドでは、エイリアス フィールドで検索を実行します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-188">If an alias field exists, the validateField method performs a lookup on the alias field.</span></span>

### <a name="examples---aliasfor"></a><span data-ttu-id="44ed7-189">例 - aliasFor</span><span class="sxs-lookup"><span data-stu-id="44ed7-189">Examples - aliasFor</span></span>

<span data-ttu-id="44ed7-190">次の例は、フィールドのエイリアス フィールドの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-190">The following example shows the retrieval of the alias field for a field.</span></span>

```xpp
DictField df; 
fieldId   fId; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum));
if (df) 
{ 
    fId = df.aliasFor(); 
    if (0 != fId) 
    { 
        print (strfmt("Field alias: %1", fieldid2name(tablenum(CustTable), fId))); 
    } 
}
```

## <a name="method-alignment"></a><span data-ttu-id="44ed7-191">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="44ed7-191">Method alignment</span></span>

```xpp
public Alignment alignment()
```

### <a name="return-value---alignment"></a><span data-ttu-id="44ed7-192">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="44ed7-192">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="44ed7-193">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="44ed7-193">Method allowEdit</span></span>

```xpp
public boolean allowEdit()
```

### <a name="return-value---allowedit"></a><span data-ttu-id="44ed7-194">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="44ed7-194">Return Value - allowEdit</span></span>

## <a name="method-alloweditoncreate"></a><span data-ttu-id="44ed7-195">メソッド allowEditOnCreate</span><span class="sxs-lookup"><span data-stu-id="44ed7-195">Method allowEditOnCreate</span></span>

```xpp
public boolean allowEditOnCreate()
```

### <a name="return-value---alloweditoncreate"></a><span data-ttu-id="44ed7-196">戻り値 - allowEditOnCreate</span><span class="sxs-lookup"><span data-stu-id="44ed7-196">Return Value - allowEditOnCreate</span></span>

## <a name="method-aosauthorization"></a><span data-ttu-id="44ed7-197">メソッド aosAuthorization</span><span class="sxs-lookup"><span data-stu-id="44ed7-197">Method aosAuthorization</span></span>

```xpp
public boolean aosAuthorization()
```

### <a name="return-value---aosauthorization"></a><span data-ttu-id="44ed7-198">戻り値 - aosAuthorization</span><span class="sxs-lookup"><span data-stu-id="44ed7-198">Return Value - aosAuthorization</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="44ed7-199">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="44ed7-199">Method arrayIndex</span></span>

```xpp
public int arrayIndex()
```

### <a name="return-value---arrayindex"></a><span data-ttu-id="44ed7-200">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="44ed7-200">Return Value - arrayIndex</span></span>

## <a name="method-arraysize"></a><span data-ttu-id="44ed7-201">メソッド arraySize</span><span class="sxs-lookup"><span data-stu-id="44ed7-201">Method arraySize</span></span>

<span data-ttu-id="44ed7-202">フィールドの配列サイズを返します (つまり、基になる拡張データ型の配列サイズ)。</span><span class="sxs-lookup"><span data-stu-id="44ed7-202">Returns the array size for the field (in other words, the array size of the underlying extended data type).</span></span>

```xpp
public int arraySize()
```

### <a name="return-value---arraysize"></a><span data-ttu-id="44ed7-203">戻り値 - arraySize</span><span class="sxs-lookup"><span data-stu-id="44ed7-203">Return Value - arraySize</span></span>

<span data-ttu-id="44ed7-204">フィールドの配列サイズ。このフィールドが配列ではない場合は 1 です。</span><span class="sxs-lookup"><span data-stu-id="44ed7-204">The array size for the field; 1 if the field is not an array.</span></span>

### <a name="examples---arraysize"></a><span data-ttu-id="44ed7-205">例 - arraySize</span><span class="sxs-lookup"><span data-stu-id="44ed7-205">Examples - arraySize</span></span>

<span data-ttu-id="44ed7-206">次の例は、フィールドの配列サイズの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-206">The following example shows the retrieval of the array size for a field.</span></span>

```xpp
DictField df; 
Types     t; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum));  
if (df) 
{ 
    print strfmt("The arraySize is %1.", df.arraySize()); 
}
```

## <a name="method-basetype"></a><span data-ttu-id="44ed7-207">メソッド baseType</span><span class="sxs-lookup"><span data-stu-id="44ed7-207">Method baseType</span></span>

<span data-ttu-id="44ed7-208">文字列、実数、整数、日付、時刻、列挙、またはコンテナーなど、フィールドの基本型を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-208">Returns the base type of the field, such as string, real, integer, date, time, enum, or container.</span></span>

```xpp
public Types baseType()
```

### <a name="return-value---basetype"></a><span data-ttu-id="44ed7-209">戻り値 - baseType</span><span class="sxs-lookup"><span data-stu-id="44ed7-209">Return Value - baseType</span></span>

<span data-ttu-id="44ed7-210">フィールドのタイプを指定するタイプ値。</span><span class="sxs-lookup"><span data-stu-id="44ed7-210">A Types value that specifies the type of the field.</span></span>

### <a name="examples---basetype"></a><span data-ttu-id="44ed7-211">例 - baseType</span><span class="sxs-lookup"><span data-stu-id="44ed7-211">Examples - baseType</span></span>

<span data-ttu-id="44ed7-212">次の例は、フィールドの基準タイプの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-212">The following example shows the retrieval of the base type of a field.</span></span>

```xpp
DictField df;
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df)
{
    print strfmt("The field type is %1.", df.baseType());
}
```

## <a name="method-configurationkeyid"></a><span data-ttu-id="44ed7-213">メソッド configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="44ed7-213">Method configurationKeyId</span></span>

<span data-ttu-id="44ed7-214">フィールドのコンフィギュレーション キーの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-214">Returns the ID of the configuration key for the field.</span></span>

```xpp
public ConfigurationKeyId configurationKeyId()
```

### <a name="return-value---configurationkeyid"></a><span data-ttu-id="44ed7-215">戻り値 - configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="44ed7-215">Return Value - configurationKeyId</span></span>

<span data-ttu-id="44ed7-216">フィールドのコンフィギュレーション キーの ID。フィールドのコンフィギュレーション キーがない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="44ed7-216">The ID of the configuration key for the field; 0 (zero) if there is no configuration key for the field.</span></span>

### <a name="examples---configurationkeyid"></a><span data-ttu-id="44ed7-217">例 - configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="44ed7-217">Examples - configurationKeyId</span></span>

<span data-ttu-id="44ed7-218">次の例は、フィールドのコンフィギュレーション キー ID とコンフィギュレーション キー名の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-218">The following example shows the retrieval of the configuration key ID and the configuration key name for a field.</span></span>

```xpp
DictField df; 
configurationKeyId cki; 
DictConfigurationKey dck; 
df = new DictField(tablenum(BankAccountTable), fieldnum(BankAccountTable, CustPaymFeePost)); 
if (df) 
{ 
    cki = df.configurationKeyId(); 
    //    print df.helpDefined(); 
    if (0 != cki) 
    { 
        dck = new DictConfigurationKey(cki); 
        if (dck) 
        print strfmt("The configuration key is %1.", dck.name()); 
    } 
    else 
    { 
        print "No configuration key"; 
    } 
}
```

## <a name="method-datetimetimezonerulefieldname"></a><span data-ttu-id="44ed7-219">メソッド dateTimeTimeZoneRuleFieldName</span><span class="sxs-lookup"><span data-stu-id="44ed7-219">Method dateTimeTimeZoneRuleFieldName</span></span>

```xpp
public str dateTimeTimeZoneRuleFieldName([int arrayindex])
```

### <a name="parameters---datetimetimezonerulefieldname"></a><span data-ttu-id="44ed7-220">パラメーター - dateTimeTimeZoneRuleFieldName</span><span class="sxs-lookup"><span data-stu-id="44ed7-220">Parameters - dateTimeTimeZoneRuleFieldName</span></span>

<span data-ttu-id="44ed7-221">arrayindex</span><span class="sxs-lookup"><span data-stu-id="44ed7-221">arrayindex</span></span>  

### <a name="return-value---datetimetimezonerulefieldname"></a><span data-ttu-id="44ed7-222">戻り値 - dateTimeTimeZoneRuleFieldName</span><span class="sxs-lookup"><span data-stu-id="44ed7-222">Return Value - dateTimeTimeZoneRuleFieldName</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="44ed7-223">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="44ed7-223">Method displayHeight</span></span>

```xpp
public int displayHeight([boolean useDefaults])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="44ed7-224">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="44ed7-224">Parameters - displayHeight</span></span>

<span data-ttu-id="44ed7-225">useDefaults</span><span class="sxs-lookup"><span data-stu-id="44ed7-225">useDefaults</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="44ed7-226">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="44ed7-226">Return Value - displayHeight</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="44ed7-227">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="44ed7-227">Method displayLength</span></span>

```xpp
public int displayLength([boolean useDefaults])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="44ed7-228">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="44ed7-228">Parameters - displayLength</span></span>

<span data-ttu-id="44ed7-229">useDefaults</span><span class="sxs-lookup"><span data-stu-id="44ed7-229">useDefaults</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="44ed7-230">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="44ed7-230">Return Value - displayLength</span></span>

## <a name="method-enumid"></a><span data-ttu-id="44ed7-231">メソッド enumId</span><span class="sxs-lookup"><span data-stu-id="44ed7-231">Method enumId</span></span>

<span data-ttu-id="44ed7-232">フィールドが列挙型に基づいている場合は列挙型の ID を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-232">Returns the ID of the enumeration if the field is based on an enumeration.</span></span>

```xpp
public EnumId enumId()
```

### <a name="return-value---enumid"></a><span data-ttu-id="44ed7-233">戻り値 - enumId</span><span class="sxs-lookup"><span data-stu-id="44ed7-233">Return Value - enumId</span></span>

<span data-ttu-id="44ed7-234">フィールドが列挙型に基づいている場合は列挙型 ID。それ以外の場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="44ed7-234">The enumeration ID if the field is based on an enumeration; otherwise, 0 (zero).</span></span>

### <a name="examples---enumid"></a><span data-ttu-id="44ed7-235">例 - enumId</span><span class="sxs-lookup"><span data-stu-id="44ed7-235">Examples - enumId</span></span>

<span data-ttu-id="44ed7-236">次の例は、列挙型 ID と列挙型に基づくフィールドの列挙型名の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-236">The following example shows the retrieval of the enumeration ID and the enumeration name of a field that is based on an enumeration.</span></span>

```xpp
DictField df; 
DictEnum  de; 
enumId    id; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    id = df.enumId(); 
    if (0 != id) 
    { 
        de = new DictEnum(id); 
        if (de) 
        { 
            print de.name(); 
        } 
    } 
}
```

## <a name="method-flags"></a><span data-ttu-id="44ed7-237">メソッド flags</span><span class="sxs-lookup"><span data-stu-id="44ed7-237">Method flags</span></span>

<span data-ttu-id="44ed7-238">フィールドのプロパティを定義する整数を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-238">Returns an integer that defines the properties of the field.</span></span> <span data-ttu-id="44ed7-239">DBF\_MANDATORY、などのフラグ値は、DictField マクロで定義されています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-239">The flag values, such as DBF\_MANDATORY, are defined in the DictField macro.</span></span>

```xpp
public int flags([str ext], [Common record])
```

### <a name="parameters---flags"></a><span data-ttu-id="44ed7-240">パラメーター - flags</span><span class="sxs-lookup"><span data-stu-id="44ed7-240">Parameters - flags</span></span>

<span data-ttu-id="44ed7-241">ext</span><span class="sxs-lookup"><span data-stu-id="44ed7-241">ext</span></span>  

<!-- -->

<span data-ttu-id="44ed7-242">記録</span><span class="sxs-lookup"><span data-stu-id="44ed7-242">record</span></span>  

### <a name="return-value---flags"></a><span data-ttu-id="44ed7-243">戻り値 - flags</span><span class="sxs-lookup"><span data-stu-id="44ed7-243">Return Value - flags</span></span>

<span data-ttu-id="44ed7-244">各ビットが、フィールド フラグに対応している整数値。</span><span class="sxs-lookup"><span data-stu-id="44ed7-244">An integer value, where each bit corresponds to a field flag.</span></span>

### <a name="remarks---flags"></a><span data-ttu-id="44ed7-245">備考 - flags</span><span class="sxs-lookup"><span data-stu-id="44ed7-245">Remarks - flags</span></span>

<span data-ttu-id="44ed7-246">Global::bitTest メソッドまたは & 演算子を使用して、個々のフラグ値を確認します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-246">Use the Global::bitTest Method method or the & operator to check individual flag values.</span></span>

### <a name="examples---flags"></a><span data-ttu-id="44ed7-247">例 - flags</span><span class="sxs-lookup"><span data-stu-id="44ed7-247">Examples - flags</span></span>

<span data-ttu-id="44ed7-248">次の例は、フィールドが必須かどうかを判断するためにフィールドのフラグを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-248">The following example shows the retrieval of the flags of a field to determine whether the field is mandatory.</span></span>

```xpp
macrolib.dictfield 
DictField df; 
int       nFlags; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    nFlags = df.flags(); 
    if (bitTest(nFlags,#DBF_MANDATORY)) 
    { 
        print ("The field is mandatory."); 
    } 
    else 
    { 
        print ("The field is not mandatory."); 
    } 
}
```

## <a name="method-getcountryregioncodes"></a><span data-ttu-id="44ed7-249">メソッド getCountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="44ed7-249">Method getCountryRegionCodes</span></span>

```xpp
public container getCountryRegionCodes()
```

### <a name="return-value---getcountryregioncodes"></a><span data-ttu-id="44ed7-250">戻り値 - getCountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="44ed7-250">Return Value - getCountryRegionCodes</span></span>

## <a name="method-getcountryregioncontextfield"></a><span data-ttu-id="44ed7-251">メソッド getCountryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="44ed7-251">Method getCountryRegionContextField</span></span>

```xpp
public FieldId getCountryRegionContextField()
```

### <a name="return-value---getcountryregioncontextfield"></a><span data-ttu-id="44ed7-252">戻り値 - getCountryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="44ed7-252">Return Value - getCountryRegionContextField</span></span>

## <a name="method-getprimarytableforsurrogatefield"></a><span data-ttu-id="44ed7-253">メソッド getPrimaryTableForSurrogateField</span><span class="sxs-lookup"><span data-stu-id="44ed7-253">Method getPrimaryTableForSurrogateField</span></span>

```xpp
public str getPrimaryTableForSurrogateField()
```

### <a name="return-value---getprimarytableforsurrogatefield"></a><span data-ttu-id="44ed7-254">戻り値 - getPrimaryTableForSurrogateField</span><span class="sxs-lookup"><span data-stu-id="44ed7-254">Return Value - getPrimaryTableForSurrogateField</span></span>

## <a name="method-groupprompt"></a><span data-ttu-id="44ed7-255">メソッド groupPrompt</span><span class="sxs-lookup"><span data-stu-id="44ed7-255">Method groupPrompt</span></span>

<span data-ttu-id="44ed7-256">フィールドの groupPrompt 値を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-256">Returns the groupPrompt value for the field.</span></span>

```xpp
public str groupPrompt()
```

### <a name="return-value---groupprompt"></a><span data-ttu-id="44ed7-257">戻り値 - groupPrompt</span><span class="sxs-lookup"><span data-stu-id="44ed7-257">Return Value - groupPrompt</span></span>

<span data-ttu-id="44ed7-258">フィールドの groupPrompt 値。</span><span class="sxs-lookup"><span data-stu-id="44ed7-258">The groupPrompt value for the field.</span></span>

## <a name="method-grouppromptdefined"></a><span data-ttu-id="44ed7-259">メソッド groupPromptDefined</span><span class="sxs-lookup"><span data-stu-id="44ed7-259">Method groupPromptDefined</span></span>

<span data-ttu-id="44ed7-260">フィールドの groupPrompt プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-260">Returns the value of the groupPrompt property for the field.</span></span>

```xpp
public str groupPromptDefined()
```

### <a name="return-value---grouppromptdefined"></a><span data-ttu-id="44ed7-261">戻り値 - groupPromptDefined</span><span class="sxs-lookup"><span data-stu-id="44ed7-261">Return Value - groupPromptDefined</span></span>

<span data-ttu-id="44ed7-262">テーブルに対する groupPrompt プロパティの値。</span><span class="sxs-lookup"><span data-stu-id="44ed7-262">The value of the groupPrompt property for the table.</span></span>

## <a name="method-help"></a><span data-ttu-id="44ed7-263">メソッド help</span><span class="sxs-lookup"><span data-stu-id="44ed7-263">Method help</span></span>

<span data-ttu-id="44ed7-264">フィールドについて表示されるヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-264">Returns the Help text that is displayed for the field.</span></span>

```xpp
public str help([int arrayIndex], [boolean useInterfaceLanguage])
```

### <a name="parameters---help"></a><span data-ttu-id="44ed7-265">パラメーター - help</span><span class="sxs-lookup"><span data-stu-id="44ed7-265">Parameters - help</span></span>

<span data-ttu-id="44ed7-266">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="44ed7-266">arrayIndex</span></span>  
<span data-ttu-id="44ed7-267">ヘルプ テキストにユーザー インターフェイス言語を使用するかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="44ed7-267">A Boolean value that indicates whether to use the user interface language for the Help text; optional.</span></span>

<!-- -->

<span data-ttu-id="44ed7-268">useInterfaceLanguage</span><span class="sxs-lookup"><span data-stu-id="44ed7-268">useInterfaceLanguage</span></span>  
<span data-ttu-id="44ed7-269">ヘルプ テキストにユーザー インターフェイス言語を使用するかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="44ed7-269">A Boolean value that indicates whether to use the user interface language for the Help text; optional.</span></span>

### <a name="return-value---help"></a><span data-ttu-id="44ed7-270">戻り値 - help</span><span class="sxs-lookup"><span data-stu-id="44ed7-270">Return Value - help</span></span>

<span data-ttu-id="44ed7-271">ヘルプ テキストまたはフィールドの継承されたヘルプ テキスト。</span><span class="sxs-lookup"><span data-stu-id="44ed7-271">The Help text or inherited Help text for the field.</span></span>

### <a name="remarks---help"></a><span data-ttu-id="44ed7-272">備考 - help</span><span class="sxs-lookup"><span data-stu-id="44ed7-272">Remarks - help</span></span>

<span data-ttu-id="44ed7-273">フィールドのヘルプ テキストが定義されていない場合、該当する場合に、このメソッドはフィールドに使用される、拡張データ型のヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-273">If no Help text is defined for the field, this method returns the Help text for the extended data type that is used for the field, if applicable.</span></span> <span data-ttu-id="44ed7-274">配列のエントリが指定されている場合、このメソッドは、配列要素のヘルプ テキストを返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-274">If an array entry is specified, this method returns the Help text for the array element.</span></span>

### <a name="examples---help"></a><span data-ttu-id="44ed7-275">例 - help</span><span class="sxs-lookup"><span data-stu-id="44ed7-275">Examples - help</span></span>

<span data-ttu-id="44ed7-276">次の例は、フィールドのヘルプ テキストの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-276">The following example shows retrieval of the Help text for the field.</span></span>

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print df.help(); 
}
```

## <a name="method-helpdefined"></a><span data-ttu-id="44ed7-277">メソッド helpDefined</span><span class="sxs-lookup"><span data-stu-id="44ed7-277">Method helpDefined</span></span>

<span data-ttu-id="44ed7-278">フィールドの help プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-278">Returns the value of the help property for the field.</span></span>

```xpp
public str helpDefined()
```

### <a name="return-value---helpdefined"></a><span data-ttu-id="44ed7-279">戻り値 - helpDefined</span><span class="sxs-lookup"><span data-stu-id="44ed7-279">Return Value - helpDefined</span></span>

<span data-ttu-id="44ed7-280">フィールドに対する help プロパティの値。</span><span class="sxs-lookup"><span data-stu-id="44ed7-280">The value of the help property for the field.</span></span>

### <a name="remarks---helpdefined"></a><span data-ttu-id="44ed7-281">備考 - helpDefined</span><span class="sxs-lookup"><span data-stu-id="44ed7-281">Remarks - helpDefined</span></span>

<span data-ttu-id="44ed7-282">ヘルプ メソッドとは異なり、フィールドが拡張データ型に基づいていて、ヘルプ テキストが定義されていない場合、helpDefined メソッドは拡張データ型のヘルプ テキストを返しません。</span><span class="sxs-lookup"><span data-stu-id="44ed7-282">Unlike the help method, the helpDefined method does not return the Help text of the extended data type if the field is based on an extended data type and has no Help text defined for it.</span></span>

### <a name="examples---helpdefined"></a><span data-ttu-id="44ed7-283">例 - helpDefined</span><span class="sxs-lookup"><span data-stu-id="44ed7-283">Examples - helpDefined</span></span>

<span data-ttu-id="44ed7-284">次の例は、フィールドの定義済ヘルプ テキストの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-284">The following example shows retrieval of the defined Help text for the field.</span></span>

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print df.helpDefined(); 
}
```

## <a name="method-id"></a><span data-ttu-id="44ed7-285">メソッド id</span><span class="sxs-lookup"><span data-stu-id="44ed7-285">Method id</span></span>

<span data-ttu-id="44ed7-286">フィールドの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-286">Returns the ID of the field.</span></span>

```xpp
public FieldId id()
```

### <a name="return-value---id"></a><span data-ttu-id="44ed7-287">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="44ed7-287">Return Value - id</span></span>

<span data-ttu-id="44ed7-288">フィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="44ed7-288">The ID of the field.</span></span>

### <a name="examples---id"></a><span data-ttu-id="44ed7-289">例 - id</span><span class="sxs-lookup"><span data-stu-id="44ed7-289">Examples - id</span></span>

<span data-ttu-id="44ed7-290">次の例では、フィールドの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-290">The following example retrieves the ID of a field.</span></span>

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print df.id(); 
}
```

## <a name="method-isignoreedtrelation"></a><span data-ttu-id="44ed7-291">メソッド isIgnoreEDTRelation</span><span class="sxs-lookup"><span data-stu-id="44ed7-291">Method isIgnoreEDTRelation</span></span>

```xpp
public boolean isIgnoreEDTRelation()
```

### <a name="return-value---isignoreedtrelation"></a><span data-ttu-id="44ed7-292">戻り値 - isIgnoreEDTRelation</span><span class="sxs-lookup"><span data-stu-id="44ed7-292">Return Value - isIgnoreEDTRelation</span></span>

## <a name="method-ismonocased"></a><span data-ttu-id="44ed7-293">メソッド isMonocased</span><span class="sxs-lookup"><span data-stu-id="44ed7-293">Method isMonocased</span></span>

<span data-ttu-id="44ed7-294">フィールドが monocase であるデータベースが必要とするかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-294">Returns a value that indicates whether the database requires that the field be monocase.</span></span>

```xpp
public boolean isMonocased()
```

### <a name="return-value---ismonocased"></a><span data-ttu-id="44ed7-295">戻り値 - isMonocased</span><span class="sxs-lookup"><span data-stu-id="44ed7-295">Return Value - isMonocased</span></span>

<span data-ttu-id="44ed7-296">フィールドが monocase である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="44ed7-296">true if the field is monocase; otherwise, false.</span></span>

## <a name="method-issql"></a><span data-ttu-id="44ed7-297">メソッド isSql</span><span class="sxs-lookup"><span data-stu-id="44ed7-297">Method isSql</span></span>

<span data-ttu-id="44ed7-298">フィールドが SQL データベースにあるかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-298">Returns a value that indicates whether the field is in the SQL database.</span></span>

```xpp
public boolean isSql()
```

### <a name="return-value---issql"></a><span data-ttu-id="44ed7-299">戻り値 - isSql</span><span class="sxs-lookup"><span data-stu-id="44ed7-299">Return Value - isSql</span></span>

<span data-ttu-id="44ed7-300">フィールドが SQL データベースである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="44ed7-300">true if the field is in the SQL database; otherwise, false.</span></span>

### <a name="examples---issql"></a><span data-ttu-id="44ed7-301">例 - isSql</span><span class="sxs-lookup"><span data-stu-id="44ed7-301">Examples - isSql</span></span>

<span data-ttu-id="44ed7-302">次の例では、フィールドが SQL データベースにあるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-302">The following example determines whether the field is in the SQL database.</span></span>

```xpp
    DictField df; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df) 
    { 
    if (df.isSql()) 
    { 
        print ("Field is in SQL database"); 
    } 
    else 
    { 
        print ("Field is not in SQL database"); 
    } 
    }
```

## <a name="method-issurrogateforeignkey"></a><span data-ttu-id="44ed7-303">メソッド isSurrogateForeignKey</span><span class="sxs-lookup"><span data-stu-id="44ed7-303">Method isSurrogateForeignKey</span></span>

```xpp
public boolean isSurrogateForeignKey()
```

### <a name="return-value---issurrogateforeignkey"></a><span data-ttu-id="44ed7-304">戻り値 - isSurrogateForeignKey</span><span class="sxs-lookup"><span data-stu-id="44ed7-304">Return Value - isSurrogateForeignKey</span></span>

## <a name="method-issystem"></a><span data-ttu-id="44ed7-305">メソッド isSystem</span><span class="sxs-lookup"><span data-stu-id="44ed7-305">Method isSystem</span></span>

<span data-ttu-id="44ed7-306">フィールドがシステム フィールドかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-306">Returns a value that indicates whether the field is a system field.</span></span>

```xpp
public boolean isSystem()
```

### <a name="return-value---issystem"></a><span data-ttu-id="44ed7-307">戻り値 - isSystem</span><span class="sxs-lookup"><span data-stu-id="44ed7-307">Return Value - isSystem</span></span>

<span data-ttu-id="44ed7-308">フィールドがシステム フィールドである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="44ed7-308">true if the field is a system field; otherwise, false.</span></span>

## <a name="method-label"></a><span data-ttu-id="44ed7-309">メソッド label</span><span class="sxs-lookup"><span data-stu-id="44ed7-309">Method label</span></span>

<span data-ttu-id="44ed7-310">フィールドのラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-310">Returns the label for the field.</span></span>

```xpp
public str label([int arrayIndex])
```

### <a name="parameters---label"></a><span data-ttu-id="44ed7-311">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="44ed7-311">Parameters - label</span></span>

<span data-ttu-id="44ed7-312">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="44ed7-312">arrayIndex</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="44ed7-313">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="44ed7-313">Return Value - label</span></span>

<span data-ttu-id="44ed7-314">フィールドのラベルまたは継承されたラベル値。</span><span class="sxs-lookup"><span data-stu-id="44ed7-314">The label or inherited label value for the field.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="44ed7-315">備考 - label</span><span class="sxs-lookup"><span data-stu-id="44ed7-315">Remarks - label</span></span>

<span data-ttu-id="44ed7-316">フィールドのラベルが指定されていない場合、該当する場合に、このメソッドはフィールドに使用される、拡張データ型のラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-316">If no label is provided for the field, this method returns the label for the extended data type for the field, if applicable.</span></span> <span data-ttu-id="44ed7-317">配列のエントリが指定されている場合、このメソッドは、配列要素のラベルを返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-317">If an array entry is specified, this method returns the label for the array element.</span></span>

## <a name="method-labeldefined"></a><span data-ttu-id="44ed7-318">メソッド labelDefined</span><span class="sxs-lookup"><span data-stu-id="44ed7-318">Method labelDefined</span></span>

<span data-ttu-id="44ed7-319">フィールドの label プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-319">Returns the value of the label property for the field.</span></span>

```xpp
public str labelDefined()
```

### <a name="return-value---labeldefined"></a><span data-ttu-id="44ed7-320">戻り値 - labelDefined</span><span class="sxs-lookup"><span data-stu-id="44ed7-320">Return Value - labelDefined</span></span>

<span data-ttu-id="44ed7-321">テーブルの label プロパティの値。テーブルのラベル テキストがない場合は空の文字列。</span><span class="sxs-lookup"><span data-stu-id="44ed7-321">The value of the label property for the table; an empty string if there is no label text for the table.</span></span>

### <a name="remarks---labeldefined"></a><span data-ttu-id="44ed7-322">備考 - labelDefined</span><span class="sxs-lookup"><span data-stu-id="44ed7-322">Remarks - labelDefined</span></span>

<span data-ttu-id="44ed7-323">label メソッドとは異なり、フィールドが拡張データ型に基づいていて、ラベルが定義されていない場合、labelDefined メソッドは拡張データ型のラベルを返しません。</span><span class="sxs-lookup"><span data-stu-id="44ed7-323">Unlike the label method, the labelDefined method does not return the extended data type label if the field is based on an extended data type and has no label defined for it.</span></span>

### <a name="examples---labeldefined"></a><span data-ttu-id="44ed7-324">例 - labelDefined</span><span class="sxs-lookup"><span data-stu-id="44ed7-324">Examples - labelDefined</span></span>

<span data-ttu-id="44ed7-325">次の例は、フィールドの定義済ラベルの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-325">The following example shows the retrieval of the defined label for a field.</span></span>

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print df.labelDefined(); 
}
```

## <a name="method-mandatory"></a><span data-ttu-id="44ed7-326">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="44ed7-326">Method mandatory</span></span>

```xpp
public boolean mandatory()
```

### <a name="return-value---mandatory"></a><span data-ttu-id="44ed7-327">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="44ed7-327">Return Value - mandatory</span></span>

## <a name="method-name"></a><span data-ttu-id="44ed7-328">メソッド名</span><span class="sxs-lookup"><span data-stu-id="44ed7-328">Method name</span></span>

<span data-ttu-id="44ed7-329">フィールドの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-329">Returns the name of the field.</span></span>

```xpp
public str name([DbBackend db], [int arrayindex], [FieldNameGenerationMode generationMode], [str tableAlias])
```

### <a name="parameters---name"></a><span data-ttu-id="44ed7-330">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="44ed7-330">Parameters - name</span></span>

<span data-ttu-id="44ed7-331">db</span><span class="sxs-lookup"><span data-stu-id="44ed7-331">db</span></span>  
<span data-ttu-id="44ed7-332">テーブルのエイリアス (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="44ed7-332">The alias for the table; optional.</span></span>

<!-- -->

<span data-ttu-id="44ed7-333">arrayindex</span><span class="sxs-lookup"><span data-stu-id="44ed7-333">arrayindex</span></span>  
<span data-ttu-id="44ed7-334">テーブルのエイリアス (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="44ed7-334">The alias for the table; optional.</span></span>

<!-- -->

<span data-ttu-id="44ed7-335">generationMode</span><span class="sxs-lookup"><span data-stu-id="44ed7-335">generationMode</span></span>  
<span data-ttu-id="44ed7-336">テーブルのエイリアス (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="44ed7-336">The alias for the table; optional.</span></span>

<!-- -->

<span data-ttu-id="44ed7-337">tableAlias</span><span class="sxs-lookup"><span data-stu-id="44ed7-337">tableAlias</span></span>  
<span data-ttu-id="44ed7-338">テーブルのエイリアス (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="44ed7-338">The alias for the table; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="44ed7-339">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="44ed7-339">Return Value - name</span></span>

<span data-ttu-id="44ed7-340">フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="44ed7-340">The name of the field.</span></span>

### <a name="examples---name"></a><span data-ttu-id="44ed7-341">例 - 名前</span><span class="sxs-lookup"><span data-stu-id="44ed7-341">Examples - name</span></span>

<span data-ttu-id="44ed7-342">次の例は、フィールドの名前の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-342">The following example shows the retrieval of the name of the field.</span></span>

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print df.name(); 
}
```

## <a name="method-origin"></a><span data-ttu-id="44ed7-343">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="44ed7-343">Method origin</span></span>

```xpp
public Guid origin()
```

### <a name="return-value---origin"></a><span data-ttu-id="44ed7-344">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="44ed7-344">Return Value - origin</span></span>

## <a name="method-qualifiedlabel"></a><span data-ttu-id="44ed7-345">メソッド qualifiedLabel</span><span class="sxs-lookup"><span data-stu-id="44ed7-345">Method qualifiedLabel</span></span>

```xpp
public str qualifiedLabel([int arrayIndex])
```

### <a name="parameters---qualifiedlabel"></a><span data-ttu-id="44ed7-346">パラメーター - qualifiedLabel</span><span class="sxs-lookup"><span data-stu-id="44ed7-346">Parameters - qualifiedLabel</span></span>

<span data-ttu-id="44ed7-347">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="44ed7-347">arrayIndex</span></span>  

### <a name="return-value---qualifiedlabel"></a><span data-ttu-id="44ed7-348">戻り値 - qualifiedLabel</span><span class="sxs-lookup"><span data-stu-id="44ed7-348">Return Value - qualifiedLabel</span></span>

## <a name="method-relatedtablename"></a><span data-ttu-id="44ed7-349">メソッド relatedTableName</span><span class="sxs-lookup"><span data-stu-id="44ed7-349">Method relatedTableName</span></span>

```xpp
public str relatedTableName()
```

### <a name="return-value---relatedtablename"></a><span data-ttu-id="44ed7-350">戻り値 - relatedTableName</span><span class="sxs-lookup"><span data-stu-id="44ed7-350">Return Value - relatedTableName</span></span>

## <a name="method-relationcontext"></a><span data-ttu-id="44ed7-351">メソッド relationContext</span><span class="sxs-lookup"><span data-stu-id="44ed7-351">Method relationContext</span></span>

```xpp
public str relationContext()
```

### <a name="return-value---relationcontext"></a><span data-ttu-id="44ed7-352">戻り値 - relationContext</span><span class="sxs-lookup"><span data-stu-id="44ed7-352">Return Value - relationContext</span></span>

## <a name="method-relationobject"></a><span data-ttu-id="44ed7-353">メソッド relationObject</span><span class="sxs-lookup"><span data-stu-id="44ed7-353">Method relationObject</span></span>

<span data-ttu-id="44ed7-354">フィールドが関係のある拡張データ型に基づいている場合、フィールドの DictRelation オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-354">Returns a DictRelation object for the field if the field is based on an extended data type that has a relation.</span></span>

```xpp
public DictRelation relationObject([int arrayIndex])
```

### <a name="parameters---relationobject"></a><span data-ttu-id="44ed7-355">パラメーター - relationObject</span><span class="sxs-lookup"><span data-stu-id="44ed7-355">Parameters - relationObject</span></span>

<span data-ttu-id="44ed7-356">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="44ed7-356">arrayIndex</span></span>  

### <a name="return-value---relationobject"></a><span data-ttu-id="44ed7-357">戻り値 - relationObject</span><span class="sxs-lookup"><span data-stu-id="44ed7-357">Return Value - relationObject</span></span>

<span data-ttu-id="44ed7-358">フィールドの関係を表す DictRelation オブジェクト。フィールドに関係が定義されていない場合、またはフィールドが拡張データ型に基づいていない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="44ed7-358">A DictRelation object that represents the relations for the field; null, Nothing, nullptr, unit, a null reference (Nothing in Visual Basic) if there no relations are defined for the field, or if the field is not based on an extended data type.</span></span>

## <a name="method-rights"></a><span data-ttu-id="44ed7-359">メソッド rights</span><span class="sxs-lookup"><span data-stu-id="44ed7-359">Method rights</span></span>

<span data-ttu-id="44ed7-360">このフィールドに指定されている、現在のユーザーのアクセス権を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-360">Returns the access rights for the current user that are specified for the field.</span></span>

```xpp
public AccessType rights([boolean ignoreContext])
```

### <a name="parameters---rights"></a><span data-ttu-id="44ed7-361">パラメーター - rights</span><span class="sxs-lookup"><span data-stu-id="44ed7-361">Parameters - rights</span></span>

<span data-ttu-id="44ed7-362">ignoreContext</span><span class="sxs-lookup"><span data-stu-id="44ed7-362">ignoreContext</span></span>  

### <a name="return-value---rights"></a><span data-ttu-id="44ed7-363">戻り値 - rights</span><span class="sxs-lookup"><span data-stu-id="44ed7-363">Return Value - rights</span></span>

<span data-ttu-id="44ed7-364">このフィールドに指定されている、現在のユーザーのアクセス権。</span><span class="sxs-lookup"><span data-stu-id="44ed7-364">The access rights for the current user that are specified for the field.</span></span>

### <a name="remarks---rights"></a><span data-ttu-id="44ed7-365">備考 - rights</span><span class="sxs-lookup"><span data-stu-id="44ed7-365">Remarks - rights</span></span>

<span data-ttu-id="44ed7-366">これは、AccessType 列挙型の値の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="44ed7-366">This can be one of the values in the AccessType enumeration.</span></span>

## <a name="method-stringlen"></a><span data-ttu-id="44ed7-367">メソッド stringLen</span><span class="sxs-lookup"><span data-stu-id="44ed7-367">Method stringLen</span></span>

<span data-ttu-id="44ed7-368">フィールドの基本型が文字列の場合、フィールドの文字列サイズを返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-368">Returns the string size of the field if the base type of the field is a string.</span></span>

```xpp
public int stringLen()
```

### <a name="return-value---stringlen"></a><span data-ttu-id="44ed7-369">戻り値 - stringLen</span><span class="sxs-lookup"><span data-stu-id="44ed7-369">Return Value - stringLen</span></span>

<span data-ttu-id="44ed7-370">フィールドの基本型が文字列の場合、フィールドの文字列サイズ。それ以外の場合は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="44ed7-370">The string size of the field if the base type of the field is a string; otherwise, 0 (zero).</span></span>

### <a name="examples---stringlen"></a><span data-ttu-id="44ed7-371">例 - stringLen</span><span class="sxs-lookup"><span data-stu-id="44ed7-371">Examples - stringLen</span></span>

<span data-ttu-id="44ed7-372">次の例は、フィールドの文字列の長さを取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-372">The following example shows retrieving the string length of a field.</span></span>

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print strfmt("The string length is %1.", df.stringLen()); 
}
```

## <a name="method-tableid"></a><span data-ttu-id="44ed7-373">メソッド tableid</span><span class="sxs-lookup"><span data-stu-id="44ed7-373">Method tableid</span></span>

<span data-ttu-id="44ed7-374">フィールドを含むテーブルの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-374">Returns the ID of the table that contains the field.</span></span>

```xpp
public TableId tableid()
```

### <a name="return-value---tableid"></a><span data-ttu-id="44ed7-375">戻り値 - tableid</span><span class="sxs-lookup"><span data-stu-id="44ed7-375">Return Value - tableid</span></span>

<span data-ttu-id="44ed7-376">フィールドを含むテーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="44ed7-376">The ID of the table that contains the field.</span></span>

### <a name="examples---tableid"></a><span data-ttu-id="44ed7-377">例 - tableid</span><span class="sxs-lookup"><span data-stu-id="44ed7-377">Examples - tableid</span></span>

<span data-ttu-id="44ed7-378">次の例は、フィールドのテーブル ID の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-378">The following example shows the retrieval of the table ID of a field.</span></span>

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print df.tableid(); 
}
```

## <a name="method-type"></a><span data-ttu-id="44ed7-379">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="44ed7-379">Method type</span></span>

<span data-ttu-id="44ed7-380">フィールドのデータ型を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-380">Returns the data type of the field.</span></span>

```xpp
public Types type()
```

### <a name="return-value---type"></a><span data-ttu-id="44ed7-381">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="44ed7-381">Return Value - type</span></span>

<span data-ttu-id="44ed7-382">フィールドのタイプを指定するタイプ値。</span><span class="sxs-lookup"><span data-stu-id="44ed7-382">A Types value that specifies the type of the field.</span></span>

### <a name="remarks---type"></a><span data-ttu-id="44ed7-383">備考 - タイプ</span><span class="sxs-lookup"><span data-stu-id="44ed7-383">Remarks - type</span></span>

<span data-ttu-id="44ed7-384">このフィールドが拡張データ型に基づいている場合は、このメソッドの戻り値として Types::UserType が返されます。</span><span class="sxs-lookup"><span data-stu-id="44ed7-384">If the field is based on an extended data type, Types::UserType is returned as the return value of this method.</span></span>

### <a name="examples---type"></a><span data-ttu-id="44ed7-385">例 - タイプ</span><span class="sxs-lookup"><span data-stu-id="44ed7-385">Examples - type</span></span>

<span data-ttu-id="44ed7-386">次の例は、フィールドのタイプの取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-386">The following example shows the retrieval of the type of a field.</span></span>

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print df.type(); 
}
```

## <a name="method-typeid"></a><span data-ttu-id="44ed7-387">メソッド typeId</span><span class="sxs-lookup"><span data-stu-id="44ed7-387">Method typeId</span></span>

<span data-ttu-id="44ed7-388">このフィールドが拡張データ型に基づいている場合は、拡張データ型の ID を返します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-388">Returns the ID of the extended data type if the field is based on an extended data type.</span></span>

```xpp
public ExtendedTypeId typeId()
```

### <a name="return-value---typeid"></a><span data-ttu-id="44ed7-389">戻り値 - typeId</span><span class="sxs-lookup"><span data-stu-id="44ed7-389">Return Value - typeId</span></span>

<span data-ttu-id="44ed7-390">フィールドが拡張データ型に基づいている場合は、拡張データ型の ID。それ以外の場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="44ed7-390">The ID of the extended data type if the field is based on an extended data type; otherwise, 0 (zero).</span></span>

### <a name="examples---typeid"></a><span data-ttu-id="44ed7-391">例 - typeId</span><span class="sxs-lookup"><span data-stu-id="44ed7-391">Examples - typeId</span></span>

<span data-ttu-id="44ed7-392">次の例は、フィールドの拡張データ型 ID の取得を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-392">The following example shows the retrieval of the extended data type ID for a field.</span></span>

```xpp
DictField df; 
extendedTypeId eti; 
DictType  dt; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
   eti = df.typeId(); 
   if (0 != eti) 
   { 
        dt = new DictType(eti); 
        if (dt) 
        { 
            print strfmt("The field is based on %1.", dt.name()); 
        } 
   } 
   else 
   { 
        print "The field is not based on an extended data type."; 
   } 
}
```

## <a name="method-visible"></a><span data-ttu-id="44ed7-393">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="44ed7-393">Method visible</span></span>

```xpp
public boolean visible()
```

### <a name="return-value---visible"></a><span data-ttu-id="44ed7-394">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="44ed7-394">Return Value - visible</span></span>

## <a name="method-setlookupmode"></a><span data-ttu-id="44ed7-395">メソッド setLookupMode</span><span class="sxs-lookup"><span data-stu-id="44ed7-395">Method setLookupMode</span></span>

```xpp
public void setLookupMode(boolean lookupMode)
```

### <a name="parameters---setlookupmode"></a><span data-ttu-id="44ed7-396">パラメーター - setLookupMode</span><span class="sxs-lookup"><span data-stu-id="44ed7-396">Parameters - setLookupMode</span></span>

<span data-ttu-id="44ed7-397">lookupMode</span><span class="sxs-lookup"><span data-stu-id="44ed7-397">lookupMode</span></span>  

## <a name="method-setsfkautoauthorizationmode"></a><span data-ttu-id="44ed7-398">メソッド setSFKAutoAuthorizationMode</span><span class="sxs-lookup"><span data-stu-id="44ed7-398">Method setSFKAutoAuthorizationMode</span></span>

```xpp
public void setSFKAutoAuthorizationMode(boolean sfkMode)
```

### <a name="parameters---setsfkautoauthorizationmode"></a><span data-ttu-id="44ed7-399">パラメーター - setSFKAutoAuthorizationMode</span><span class="sxs-lookup"><span data-stu-id="44ed7-399">Parameters - setSFKAutoAuthorizationMode</span></span>

<span data-ttu-id="44ed7-400">sfkMode</span><span class="sxs-lookup"><span data-stu-id="44ed7-400">sfkMode</span></span>  

## <a name="method-new"></a><span data-ttu-id="44ed7-401">メソッド new</span><span class="sxs-lookup"><span data-stu-id="44ed7-401">Method new</span></span>

<span data-ttu-id="44ed7-402">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="44ed7-402">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(TableId tableId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---new"></a><span data-ttu-id="44ed7-403">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="44ed7-403">Parameters - new</span></span>

<span data-ttu-id="44ed7-404">tableId</span><span class="sxs-lookup"><span data-stu-id="44ed7-404">tableId</span></span>  

<!-- -->

<span data-ttu-id="44ed7-405">fieldId</span><span class="sxs-lookup"><span data-stu-id="44ed7-405">fieldId</span></span>  

<!-- -->

<span data-ttu-id="44ed7-406">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="44ed7-406">arrayIndex</span></span>  

### <a name="examples---new"></a><span data-ttu-id="44ed7-407">例 - new</span><span class="sxs-lookup"><span data-stu-id="44ed7-407">Examples - new</span></span>

<span data-ttu-id="44ed7-408">次の例は、DictField クラスのインスタンスを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="44ed7-408">The following example shows how to create an instance of the DictField class.</span></span>

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
// Check df for successful creation before proceeding. 
if (!df) 
{ 
// Take error action. 
}
```

