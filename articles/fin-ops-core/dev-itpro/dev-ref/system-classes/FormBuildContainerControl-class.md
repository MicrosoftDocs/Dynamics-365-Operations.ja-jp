---
title: FormBuildContainerControl クラス
description: このトピックでは、FormBuildContainerControl クラスについて説明します。
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
ms.openlocfilehash: 5d8b92cb3a84409a4d98aef1b7303ab849340aad
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502971"
---
# <a name="class-formbuildcontainercontrol"></a>クラス FormBuildContainerControl

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildContainerControl extends FormBuildControl
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明 |
|-------------------------------------------------------------------------------------------------------------|-------------|
| public boolean alignControl(\[boolean value\])                                                              |             |
| public boolean allowEdit(\[boolean value\])                                                                 |             |
| public boolean autoDeclaration(\[boolean value\])                                                           |             |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    |             |
| public int containerId()                                                                                    |             |
| public str countryRegionCodes(\[str value\])                                                                |             |
| public str dataRelationPath(\[str value\])                                                                  |             |
| public int displayTarget(\[int value\])                                                                     |             |
| public int dragDrop(\[int value\])                                                                          |             |
| public boolean enabled(\[boolean value\])                                                                   |             |
| public int height(int value, \[int mode\])                                                                  |             |
| public int heightMode(\[int value\])                                                                        |             |
| public int heightValue(\[int value\])                                                                       |             |
| public str helpText(\[str value\])                                                                          |             |
| public str hierarchyParent(\[str value\])                                                                   |             |
| public int id()                                                                                             |             |
| public boolean isContainer()                                                                                |             |
| public int left(int value, \[int mode\])                                                                    |             |
| public int leftMode(\[int value\])                                                                          |             |
| public int leftValue(\[int value\])                                                                         |             |
| public int moveControl(int controlId, \[int insertAfterControlId\])                                         |             |
| public str name(\[str value\])                                                                              |             |
| public int neededPermission(\[int value\])                                                                  |             |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |             |
| public boolean skip(\[boolean value\])                                                                      |             |
| public int top(int value, \[int mode\])                                                                     |             |
| public int topMode(\[int value\])                                                                           |             |
| public int topValue(\[int value\])                                                                          |             |
| public int type(\[int value\])                                                                              |             |
| public int userData(\[int value\])                                                                          |             |
| public int userDataItem(\[int value\])                                                                      |             |
| public int userDataItems(\[int value\])                                                                     |             |
| public boolean useUserLayout(\[boolean value\])                                                             |             |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |             |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |             |
| public int verticalSpacingValue(\[int value\])                                                              |             |
| public boolean visible(\[boolean value\])                                                                   |             |
| public int width(int value, \[int mode\])                                                                   |             |
| public int widthMode(\[int value\])                                                                         |             |
| public int widthValue(\[int value\])                                                                        |             |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |             |

## <a name="method-aligncontrol"></a>メソッド alignControl

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a>パラメーター - alignControl

値  

### <a name="return-value---aligncontrol"></a>戻り値 - alignControl

## <a name="method-allowedit"></a>メソッド allowEdit

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a>パラメーター - allowEdit

値  

### <a name="return-value---allowedit"></a>戻り値 - allowEdit

## <a name="method-autodeclaration"></a>メソッド autoDeclaration

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a>パラメーター - autoDeclaration

値  

### <a name="return-value---autodeclaration"></a>戻り値 - autoDeclaration

## <a name="method-configurationkey"></a>メソッド configurationKey

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a>パラメーター - configurationKey

値  

### <a name="return-value---configurationkey"></a>戻り値 - configurationKey

## <a name="method-containerid"></a>メソッド containerId

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a>戻り値 - containerId

## <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a>パラメーター - countryRegionCodes

値  

### <a name="return-value---countryregioncodes"></a>戻り値 - countryRegionCodes

## <a name="method-datarelationpath"></a>メソッド dataRelationPath

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a>パラメーター - dataRelationPath

値  

### <a name="return-value---datarelationpath"></a>戻り値 - dataRelationPath

## <a name="method-displaytarget"></a>メソッド displayTarget

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a>パラメーター - displayTarget

値  

### <a name="return-value---displaytarget"></a>戻り値 - displayTarget

## <a name="method-dragdrop"></a>メソッド dragDrop

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a>パラメーター - dragDrop

値  

### <a name="return-value---dragdrop"></a>戻り値 - dragDrop

## <a name="method-enabled"></a>メソッド enabled

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a>パラメーター - enabled

値  

### <a name="return-value---enabled"></a>戻り値 - enabled

## <a name="method-height"></a>メソッド height

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a>パラメーター - height

値  

<!-- -->

モード  

### <a name="return-value---height"></a>戻り値 - height

## <a name="method-heightmode"></a>メソッド heightMode

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a>パラメーター - heightMode

値  

### <a name="return-value---heightmode"></a>戻り値 - heightMode

## <a name="method-heightvalue"></a>メソッド heightValue

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a>パラメーター - heightValue

値  

### <a name="return-value---heightvalue"></a>戻り値 - heightValue

## <a name="method-helptext"></a>メソッド helpText

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a>パラメーター - helpText

値  

### <a name="return-value---helptext"></a>戻り値 - helpText

## <a name="method-hierarchyparent"></a>メソッド hierarchyParent

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a>パラメーター - hierarchyParent

値  

### <a name="return-value---hierarchyparent"></a>戻り値 - hierarchyParent

## <a name="method-id"></a>メソッド id

```xpp
public int id()
```

### <a name="return-value---id"></a>戻り値 - id

## <a name="method-iscontainer"></a>メソッド isContainer

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a>戻り値 - isContainer

## <a name="method-left"></a>メソッド left

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a>パラメーター - left

値  

<!-- -->

モード  

### <a name="return-value---left"></a>戻り値 - left

## <a name="method-leftmode"></a>メソッド leftMode

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a>パラメーター - leftMode

値  

### <a name="return-value---leftmode"></a>戻り値 - leftMode

## <a name="method-leftvalue"></a>メソッド leftValue

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a>パラメーター - leftValue

値  

### <a name="return-value---leftvalue"></a>戻り値 - leftValue

## <a name="method-movecontrol"></a>メソッド moveControl

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a>パラメーター - moveControl

controlId  

<!-- -->

insertAfterControlId  

### <a name="return-value---movecontrol"></a>戻り値 - moveControl

## <a name="method-name"></a>メソッド名

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - 名前

値  

### <a name="return-value---name"></a>戻り値 - name

## <a name="method-neededpermission"></a>メソッド neededPermission

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a>パラメーター - neededPermission

値  

### <a name="return-value---neededpermission"></a>戻り値 - neededPermission

## <a name="method-securitykey"></a>メソッド securityKey

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a>パラメーター - securityKey

値  

### <a name="return-value---securitykey"></a>戻り値 - securityKey

## <a name="method-skip"></a>メソッド skip

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a>パラメーター - skip

値  

### <a name="return-value---skip"></a>戻り値 - skip

## <a name="method-top"></a>メソッド top

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a>パラメーター - top

値  

<!-- -->

モード  

### <a name="return-value---top"></a>戻り値 - top

## <a name="method-topmode"></a>メソッド topMode

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a>パラメーター - topMode

値  

### <a name="return-value---topmode"></a>戻り値 - topMode

## <a name="method-topvalue"></a>メソッド topValue

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a>パラメーター - topValue

値  

### <a name="return-value---topvalue"></a>戻り値 - topValue

## <a name="method-type"></a>メソッドのタイプ

```xpp
public int type([int value])
```

### <a name="parameters---type"></a>パラメーター - タイプ

値  

### <a name="return-value---type"></a>戻り値 - type

## <a name="method-userdata"></a>メソッド userData

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a>パラメーター - userData

値  

### <a name="return-value---userdata"></a>戻り値 - userData

## <a name="method-userdataitem"></a>メソッド userDataItem

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a>パラメーター - userDataItem

値  

### <a name="return-value---userdataitem"></a>戻り値 - userDataItem

## <a name="method-userdataitems"></a>メソッド userDataItems

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a>パラメーター - userDataItems

値  

### <a name="return-value---userdataitems"></a>戻り値 - userDataItems

## <a name="method-useuserlayout"></a>メソッド useUserLayout

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a>パラメーター - useUserLayout

値  

### <a name="return-value---useuserlayout"></a>戻り値 - useUserLayout

## <a name="method-verticalspacing"></a>メソッド verticalSpacing

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a>パラメーター - verticalSpacing

値  

<!-- -->

モード  

### <a name="return-value---verticalspacing"></a>戻り値 - verticalSpacing

## <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a>パラメーター - verticalSpacingMode

モード  

### <a name="return-value---verticalspacingmode"></a>戻り値 - verticalSpacingMode

## <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a>パラメーター - verticalSpacingValue

値  

### <a name="return-value---verticalspacingvalue"></a>戻り値 - verticalSpacingValue

## <a name="method-visible"></a>メソッド visible

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a>パラメーター - visible

値  

### <a name="return-value---visible"></a>戻り値 - visible

## <a name="method-width"></a>メソッド width

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a>パラメーター - width

値  

<!-- -->

モード  

### <a name="return-value---width"></a>戻り値 - width

## <a name="method-widthmode"></a>メソッド widthMode

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a>パラメーター - widthValue

値  

### <a name="return-value---widthmode"></a>戻り値 - widthMode

## <a name="method-widthvalue"></a>メソッド widthValue

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a>パラメーター - widthValue

値  

### <a name="return-value---widthvalue"></a>戻り値 - widthValue

## <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a>パラメーター - registerOverrideMethod

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

