---
title: FormContainerControl クラス
description: このトピックでは、FormContainerControl クラスについて説明します。
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
ms.openlocfilehash: 456d2eab0576f6dfdc94cba489851c97f49db519
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502636"
---
# <a name="class-formcontainercontrol"></a>クラス FormContainerControl

[!include [banner](../../includes/banner.md)]

```xpp
class FormContainerControl extends FormControl
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                              | 説明 |
|---------------------------------------------------------------------------------------------------------------------|-------------|
| public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])            |             |
| public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])                     |             |
| public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\]) |             |
| public boolean alignChild(\[boolean value\])                                                                        |             |
| public boolean alignChildren(\[boolean value\])                                                                     |             |
| public boolean alignControl(\[boolean value\])                                                                      |             |
| public boolean allowEdit(\[boolean value\])                                                                         |             |
| public boolean allowSysSetup()                                                                                      |             |
| public int allowUserSetup(\[int value\])                                                                            |             |
| public int arrangeGuide(\[int value\])                                                                              |             |
| public int arrangeMethod(\[int value\])                                                                             |             |
| public int arrangeWhen(\[int value\])                                                                               |             |
| public boolean autoDataGroup(\[boolean value\])                                                                     |             |
| public boolean autoDeclaration(\[boolean value\])                                                                   |             |
| public int beginDrag(int x, int y)                                                                                  |             |
| public int bottomMargin(\[int value\], \[AutoMode mode\])                                                           |             |
| public AutoMode bottomMarginMode(\[AutoMode mode\])                                                                 |             |
| public int bottomMarginValue(\[int value\])                                                                         |             |
| public container calcControlSize(int chars, int lines)                                                              |             |
| public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])                               |             |
| public boolean canContain(FormControl control)                                                                      |             |
| public int columns(\[int value\], \[ColumnsMode mode\])                                                             |             |
| public ColumnsMode columnsMode(\[ColumnsMode mode\])                                                                |             |
| public int columnspace(\[int value\], \[AutoMode mode\])                                                            |             |
| public AutoMode columnspaceMode(\[AutoMode mode\])                                                                  |             |
| public int columnspaceValue(\[int value\])                                                                          |             |
| public int columnsValue(\[int value\])                                                                              |             |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                            |             |
| public List configurationKeyEx()                                                                                    |             |
| public boolean contains(FormControl control)                                                                        |             |
| public int controlCount()                                                                                           |             |
| public FormControl controlNum(int controlNo)                                                                        |             |
| public str countryRegionCodes(\[str value\])                                                                        |             |
| public str dataRelationPath(\[str value\])                                                                          |             |
| public int displayTarget(\[int value\])                                                                             |             |
| public int dragDrop(\[int value\])                                                                                  |             |
| public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)                                   |             |
| public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)                                       |             |
| public str dragText()                                                                                               |             |
| public boolean enabled(\[boolean value\])                                                                           |             |
| public boolean hasChanged(\[boolean val\])                                                                          |             |
| public boolean hasUserSetting()                                                                                     |             |
| public int height(int value, \[int mode\])                                                                          |             |
| public int heightMode(\[int value\])                                                                                |             |
| public int heightValue(\[int value\])                                                                               |             |
| public str helpField()                                                                                              |             |
| public str helpText(\[str value\])                                                                                  |             |
| public boolean hideIfEmpty(\[boolean value\])                                                                       |             |
| public str hierarchyParent(\[str value\])                                                                           |             |
| public int hWnd()                                                                                                   |             |
| public boolean isContainer()                                                                                        |             |
| public boolean isDisplayed()                                                                                        |             |
| public boolean isRestricted()                                                                                       |             |
| public boolean isUserSetupEnabled(int neededSetupRights)                                                            |             |
| public boolean isVisible()                                                                                          |             |
| public boolean isVisibleOnClient()                                                                                  |             |
| public int left(int value, \[int mode\])                                                                            |             |
| public int leftMargin(\[int value\], \[AutoMode mode\])                                                             |             |
| public AutoMode leftMarginMode(\[AutoMode mode\])                                                                   |             |
| public int leftMarginValue(\[int value\])                                                                           |             |
| public int leftMode(\[int value\])                                                                                  |             |
| public int leftValue(\[int value\])                                                                                 |             |
| public boolean markAsUserAdd(\[boolean value\])                                                                     |             |
| public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)                                     |             |
| public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)                                         |             |
| public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)                                         |             |
| public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)                                           |             |
| public int moveControl(int controlId, \[int insertAfterId\])                                                        |             |
| public str name(\[str value\])                                                                                      |             |
| public int neededPermission(\[int value\])                                                                          |             |
| public container SysObsoleteAttribute()                                                                             |             |
| public FormControl parentControl()                                                                                  |             |
| public int rightMargin(\[int value\], \[AutoMode mode\])                                                            |             |
| public AutoMode rightMarginMode(\[AutoMode mode\])                                                                  |             |
| public int rightMarginValue(\[int value\])                                                                          |             |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                           |             |
| public int showContextMenu(int menuHandle)                                                                          |             |
| public boolean skip(\[boolean value\])                                                                              |             |
| public str toolTip()                                                                                                |             |
| public int top(int value, \[int mode\])                                                                             |             |
| public int topMargin(\[int value\], \[AutoMode mode\])                                                              |             |
| public AutoMode topMarginMode(\[AutoMode mode\])                                                                    |             |
| public int topMarginValue(\[int value\])                                                                            |             |
| public int topMode(\[int value\])                                                                                   |             |
| public int topValue(\[int value\])                                                                                  |             |
| public int type(\[int value\])                                                                                      |             |
| public boolean SysObsoleteAttribute(container data)                                                                 |             |
| public int userData(\[int value\])                                                                                  |             |
| public int userDataItem(\[int value\])                                                                              |             |
| public int userDataItems(\[int value\])                                                                             |             |
| public int userDisable(\[int value\])                                                                               |             |
| public int userHeight(\[int value\])                                                                                |             |
| public int userHide(\[int value\])                                                                                  |             |
| public int userOrgContainer(\[int value\])                                                                          |             |
| public int userOrgSibling(\[int value\])                                                                            |             |
| public str userPromptText(\[str value\])                                                                            |             |
| public int userSecurityLevel(\[int value\])                                                                         |             |
| public int userSkip(\[int value\])                                                                                  |             |
| public int userWidth(\[int value\])                                                                                 |             |
| public boolean useUserLayout(\[boolean value\])                                                                     |             |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                        |             |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                              |             |
| public int verticalSpacingValue(\[int value\])                                                                      |             |
| public boolean visible(\[boolean value\])                                                                           |             |
| public int width(int value, \[int mode\])                                                                           |             |
| public int widthMode(\[int value\])                                                                                 |             |
| public int widthValue(\[int value\])                                                                                |             |
| public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)                                               |             |
| public void inputSearch(str searchStr)                                                                              |             |
| public void prefColumnSize(int width, int height)                                                                   |             |
| public void gotFocus()                                                                                              |             |
| public void lostFocus()                                                                                             |             |
| public void mouseLeave()                                                                                            |             |
| public void setFocus()                                                                                              |             |
| public void copy()                                                                                                  |             |
| private void OnGotFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                         |             |
| public void displayControl()                                                                                        |             |
| public void paste()                                                                                                 |             |
| public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)                                           |             |
| private void OnLostFocus(\[FormControl sender\], \[FormControlEventArgs e\])                                        |             |
| public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)                                       |             |
| public void resetUserSetting()                                                                                      |             |
| public void endDrag()                                                                                               |             |
| public void arrange()                                                                                               |             |
| public void dragLeave()                                                                                             |             |
| public void cut()                                                                                                   |             |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])         |             |
| public void context()                                                                                               |             |

## <a name="method-addcontrol"></a>メソッド addControl

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a>パラメーター - addControl

controlType  

<!-- -->

controlName  

<!-- -->

insertAfter  

### <a name="return-value---addcontrol"></a>戻り値 - addControl

## <a name="method-addcontrolex"></a>メソッド addControlEx

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a>パラメーター - addControlEx

controlClass  

<!-- -->

controlName  

<!-- -->

insertAfter  

### <a name="return-value---addcontrolex"></a>戻り値 - addControlEx

## <a name="method-adddatafield"></a>メソッド addDataField

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a>パラメーター - addDataField

dataSourceId  

<!-- -->

fieldId  

<!-- -->

insertAfter  

<!-- -->

arrayIndex  

### <a name="return-value---adddatafield"></a>戻り値 - addDataField

## <a name="method-alignchild"></a>メソッド alignChild

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a>パラメーター - alignChild

値  

### <a name="return-value---alignchild"></a>戻り値 - alignChild

## <a name="method-alignchildren"></a>メソッド alignChildren

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a>パラメーター - alignChildren

値  

### <a name="return-value---alignchildren"></a>戻り値 - alignChildren

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

## <a name="method-allowsyssetup"></a>メソッド allowSysSetup

```xpp
public boolean allowSysSetup()
```

### <a name="return-value---allowsyssetup"></a>戻り値 - allowSysSetup

## <a name="method-allowusersetup"></a>メソッド allowUserSetup

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a>パラメーター - allowUserSetup

値  

### <a name="return-value---allowusersetup"></a>戻り値 - allowUserSetup

## <a name="method-arrangeguide"></a>メソッド arrangeGuide

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a>パラメーター - arrangeGuide

値  

### <a name="return-value---arrangeguide"></a>戻り値 - arrangeGuide

## <a name="method-arrangemethod"></a>メソッド arrangeMethod

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a>パラメーター - arrangeMethod

値  

### <a name="return-value---arrangemethod"></a>戻り値 - arrangeMethod

## <a name="method-arrangewhen"></a>メソッド arrangeWhen

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a>パラメーター - arrangeWhen

値  

### <a name="return-value---arrangewhen"></a>戻り値 - arrangeWhen

## <a name="method-autodatagroup"></a>メソッド autoDataGroup

```xpp
public boolean autoDataGroup([boolean value])
```

### <a name="parameters---autodatagroup"></a>パラメーター - autoDataGroup

値  

### <a name="return-value---autodatagroup"></a>戻り値 - autoDataGroup

## <a name="method-autodeclaration"></a>メソッド autoDeclaration

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a>パラメーター - autoDeclaration

値  

### <a name="return-value---autodeclaration"></a>戻り値 - autoDeclaration

## <a name="method-begindrag"></a>メソッド beginDrag

```xpp
public int beginDrag(int x, int y)
```

### <a name="parameters---begindrag"></a>パラメーター - beginDrag

x  

<!-- -->

y  

### <a name="return-value---begindrag"></a>戻り値 - beginDrag

## <a name="method-bottommargin"></a>メソッド bottomMargin

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a>パラメーター - bottomMargin

値  

<!-- -->

モード  

### <a name="return-value---bottommargin"></a>戻り値 - bottomMargin

## <a name="method-bottommarginmode"></a>メソッド bottomMarginMode

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a>パラメーター - bottomMarginMode

モード  

### <a name="return-value---bottommarginmode"></a>戻り値 - bottomMarginMode

## <a name="method-bottommarginvalue"></a>メソッド bottomMarginValue

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a>パラメーター - bottomMarginValue

値  

### <a name="return-value---bottommarginvalue"></a>戻り値 - bottomMarginValue

## <a name="method-calccontrolsize"></a>メソッド calcControlSize

```xpp
public container calcControlSize(int chars, int lines)
```

### <a name="parameters---calccontrolsize"></a>パラメーター - calcControlSize

chars  

<!-- -->

明細行  

### <a name="return-value---calccontrolsize"></a>戻り値 - calcControlSize

## <a name="method-canadddatafield"></a>メソッド canAddDataField

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a>パラメーター - canAddDataField

dataSourceId  

<!-- -->

fieldId  

<!-- -->

arrayIndex  

### <a name="return-value---canadddatafield"></a>戻り値 - canAddDataField

## <a name="method-cancontain"></a>メソッド canContain

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a>パラメーター - canContain

control  

### <a name="return-value---cancontain"></a>戻り値 - canContain

## <a name="method-columns"></a>メソッド columns

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a>パラメーター - columns

値  

<!-- -->

モード  

### <a name="return-value---columns"></a>戻り値 - columns

## <a name="method-columnsmode"></a>メソッド columnsMode

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a>パラメーター - columnsMode

モード  

### <a name="return-value---columnsmode"></a>戻り値 - columnsMode

## <a name="method-columnspace"></a>メソッド columnspace

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a>パラメーター - columnspace

値  

<!-- -->

モード  

### <a name="return-value---columnspace"></a>戻り値 - columnspace

## <a name="method-columnspacemode"></a>メソッド columnspaceMode

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a>パラメーター - columnspaceMode

モード  

### <a name="return-value---columnspacemode"></a>戻り値 - columnspaceMode

## <a name="method-columnspacevalue"></a>メソッド columnspaceValue

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a>パラメーター - columnspaceValue

値  

### <a name="return-value---columnspacevalue"></a>戻り値 - columnspaceValue

## <a name="method-columnsvalue"></a>メソッド columnsValue

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a>パラメーター - columnsValue

値  

### <a name="return-value---columnsvalue"></a>戻り値 - columnsValue

## <a name="method-configurationkey"></a>メソッド configurationKey

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a>パラメーター - configurationKey

値  

### <a name="return-value---configurationkey"></a>戻り値 - configurationKey

## <a name="method-configurationkeyex"></a>メソッド configurationKeyEx

```xpp
public List configurationKeyEx()
```

### <a name="return-value---configurationkeyex"></a>戻り値 - configurationKeyEx

## <a name="method-contains"></a>メソッド contains

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a>パラメーター - contains

control  

### <a name="return-value---contains"></a>戻り値 - contains

## <a name="method-controlcount"></a>メソッド controlCount

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a>戻り値 - controlCount

## <a name="method-controlnum"></a>メソッド controlNum

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a>パラメーター - controlNum

controlNo  

### <a name="return-value---controlnum"></a>戻り値 - controlNum

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

## <a name="method-dragover"></a>メソッド dragOver

```xpp
public FormDrag dragOver(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragover"></a>パラメーター - dragOver

dragSource  

<!-- -->

dragMode  

<!-- -->

x  

<!-- -->

y  

### <a name="return-value---dragover"></a>戻り値 - dragOver

## <a name="method-dragoverex"></a>メソッド dragOverEx

```xpp
public FormDrag dragOverEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dragoverex"></a>パラメーター - dragOverEx

dragSource  

<!-- -->

dragMode  

<!-- -->

x  

<!-- -->

y  

### <a name="return-value---dragoverex"></a>戻り値 - dragOverEx

## <a name="method-dragtext"></a>メソッド dragText

```xpp
public str dragText()
```

### <a name="return-value---dragtext"></a>戻り値 - dragText

## <a name="method-enabled"></a>メソッド enabled

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a>パラメーター - enabled

値  

### <a name="return-value---enabled"></a>戻り値 - enabled

## <a name="method-haschanged"></a>メソッド hasChanged

```xpp
public boolean hasChanged([boolean val])
```

### <a name="parameters---haschanged"></a>パラメーター - hasChanged

val  

### <a name="return-value---haschanged"></a>戻り値 - hasChanged

## <a name="method-hasusersetting"></a>メソッド hasUserSetting

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a>戻り値 - hasUserSetting

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

## <a name="method-helpfield"></a>メソッド helpField

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a>戻り値 - helpField

## <a name="method-helptext"></a>メソッド helpText

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a>パラメーター - helpText

値  

### <a name="return-value---helptext"></a>戻り値 - helpText

## <a name="method-hideifempty"></a>メソッド hideIfEmpty

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a>パラメーター - hideIfEmpty

値  

### <a name="return-value---hideifempty"></a>戻り値 - hideIfEmpty

## <a name="method-hierarchyparent"></a>メソッド hierarchyParent

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a>パラメーター - hierarchyParent

値  

### <a name="return-value---hierarchyparent"></a>戻り値 - hierarchyParent

## <a name="method-hwnd"></a>メソッド hWnd

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a>戻り値 - hWnd

## <a name="method-iscontainer"></a>メソッド isContainer

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a>戻り値 - isContainer

## <a name="method-isdisplayed"></a>メソッド isDisplayed

```xpp
public boolean isDisplayed()
```

### <a name="return-value---isdisplayed"></a>戻り値 - isDisplayed

## <a name="method-isrestricted"></a>メソッド isRestricted

```xpp
public boolean isRestricted()
```

### <a name="return-value---isrestricted"></a>戻り値 - isRestricted

## <a name="method-isusersetupenabled"></a>メソッド isUserSetupEnabled

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a>パラメーター - isUserSetupEnabled

neededSetupRights  

### <a name="return-value---isusersetupenabled"></a>戻り値 - isUserSetupEnabled

## <a name="method-isvisible"></a>メソッド isVisible

```xpp
public boolean isVisible()
```

### <a name="return-value---isvisible"></a>戻り値 - isVisible

## <a name="method-isvisibleonclient"></a>メソッド isVisibleOnClient

```xpp
public boolean isVisibleOnClient()
```

### <a name="return-value---isvisibleonclient"></a>戻り値 - isVisibleOnClient

## <a name="method-left"></a>メソッド left

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a>パラメーター - left

値  

<!-- -->

モード  

### <a name="return-value---left"></a>戻り値 - left

## <a name="method-leftmargin"></a>メソッド leftMargin

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a>パラメーター - leftMargin

値  

<!-- -->

モード  

### <a name="return-value---leftmargin"></a>戻り値 - leftMargin

## <a name="method-leftmarginmode"></a>メソッド leftMarginMode

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a>パラメーター - leftMarginMode

モード  

### <a name="return-value---leftmarginmode"></a>戻り値 - leftMarginMode

## <a name="method-leftmarginvalue"></a>メソッド leftMarginValue

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a>パラメーター - leftMarginValue

値  

### <a name="return-value---leftmarginvalue"></a>戻り値 - leftMarginValue

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

## <a name="method-markasuseradd"></a>メソッド markAsUserAdd

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a>パラメーター - markAsUserAdd

値  

### <a name="return-value---markasuseradd"></a>戻り値 - markAsUserAdd

## <a name="method-mousedblclick"></a>メソッド mouseDblClick

```xpp
public int mouseDblClick(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedblclick"></a>パラメーター - mouseDblClick

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

Shift  

### <a name="return-value---mousedblclick"></a>戻り値 - mouseDblClick

## <a name="method-mousedown"></a>メソッド mouseDown

```xpp
public int mouseDown(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousedown"></a>パラメーター - mouseDown

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

Shift  

### <a name="return-value---mousedown"></a>戻り値 - mouseDown

## <a name="method-mousemove"></a>メソッド mouseMove

```xpp
public int mouseMove(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mousemove"></a>パラメーター - mouseMove

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

Shift  

### <a name="return-value---mousemove"></a>戻り値 - mouseMove

## <a name="method-mouseup"></a>メソッド mouseUp

```xpp
public int mouseUp(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseup"></a>パラメーター - mouseUp

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

Shift  

### <a name="return-value---mouseup"></a>戻り値 - mouseUp

## <a name="method-movecontrol"></a>メソッド moveControl

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a>パラメーター - moveControl

controlId  

<!-- -->

insertAfterId  

### <a name="return-value---movecontrol"></a>戻り値 - moveControl

## <a name="method-name"></a>メソッド名

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  

### <a name="return-value---name"></a>戻り値 - name

## <a name="method-neededpermission"></a>メソッド neededPermission

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a>パラメーター - neededPermission

値  

### <a name="return-value---neededpermission"></a>戻り値 - neededPermission

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

## <a name="method-parentcontrol"></a>メソッド parentControl

```xpp
public FormControl parentControl()
```

### <a name="return-value---parentcontrol"></a>戻り値 - parentControl

## <a name="method-rightmargin"></a>メソッド rightMargin

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a>パラメーター - rightMargin

値  

<!-- -->

モード  

### <a name="return-value---rightmargin"></a>戻り値 - rightMargin

## <a name="method-rightmarginmode"></a>メソッド rightMarginMode

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a>パラメーター - rightMarginMode

モード  

### <a name="return-value---rightmarginmode"></a>戻り値 - rightMarginMode

## <a name="method-rightmarginvalue"></a>メソッド rightMarginValue

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a>パラメーター - rightMarginValue

値  

### <a name="return-value---rightmarginvalue"></a>戻り値 - rightMarginValue

## <a name="method-securitykey"></a>メソッド securityKey

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a>パラメーター - securityKey

値  

### <a name="return-value---securitykey"></a>戻り値 - securityKey

## <a name="method-showcontextmenu"></a>メソッド showContextMenu

```xpp
public int showContextMenu(int menuHandle)
```

### <a name="parameters---showcontextmenu"></a>パラメーター - showContextMenu

menuHandle  

### <a name="return-value---showcontextmenu"></a>戻り値 - showContextMenu

## <a name="method-skip"></a>メソッド skip

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a>パラメーター - skip

値  

### <a name="return-value---skip"></a>戻り値 - skip

## <a name="method-tooltip"></a>メソッド toolTip

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a>戻り値 - toolTip

## <a name="method-top"></a>メソッド top

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a>パラメーター - top

値  

<!-- -->

モード  

### <a name="return-value---top"></a>戻り値 - top

## <a name="method-topmargin"></a>メソッド topMargin

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a>パラメーター - topMargin

値  

<!-- -->

モード  

### <a name="return-value---topmargin"></a>戻り値 - topMargin

## <a name="method-topmarginmode"></a>メソッド topMarginMode

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a>パラメーター - topMarginMode

モード  

### <a name="return-value---topmarginmode"></a>戻り値 - topMarginMode

## <a name="method-topmarginvalue"></a>メソッド topMarginValue

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a>パラメーター - topMarginValue

値  

### <a name="return-value---topmarginvalue"></a>戻り値 - topMarginValue

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

### <a name="parameters---type"></a>パラメーター - type

値  

### <a name="return-value---type"></a>戻り値 - type

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

データ  

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

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

## <a name="method-userdisable"></a>メソッド userDisable

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a>パラメーター - userDisable

値  

### <a name="return-value---userdisable"></a>戻り値 - userDisable

## <a name="method-userheight"></a>メソッド userHeight

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a>パラメーター - userHeight

値  

### <a name="return-value---userheight"></a>戻り値 - userHeight

## <a name="method-userhide"></a>メソッド userHide

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a>パラメーター - userHide

値  

### <a name="return-value---userhide"></a>戻り値 - userHide

## <a name="method-userorgcontainer"></a>メソッド userOrgContainer

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a>パラメーター - userOrgContainer

値  

### <a name="return-value---userorgcontainer"></a>戻り値 - userOrgContainer

## <a name="method-userorgsibling"></a>メソッド userOrgSibling

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a>パラメーター - userOrgSibling

値  

### <a name="return-value---userorgsibling"></a>戻り値 - userOrgSibling

## <a name="method-userprompttext"></a>メソッド userPromptText

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a>パラメーター - userPromptText

値  

### <a name="return-value---userprompttext"></a>戻り値 - userPromptText

## <a name="method-usersecuritylevel"></a>メソッド userSecurityLevel

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a>パラメーター - userSecurityLevel

値  

### <a name="return-value---usersecuritylevel"></a>戻り値 - userSecurityLevel

## <a name="method-userskip"></a>メソッド userSkip

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a>パラメーター - userSkip

値  

### <a name="return-value---userskip"></a>戻り値 - userSkip

## <a name="method-userwidth"></a>メソッド userWidth

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a>パラメーター - userWidth

値  

### <a name="return-value---userwidth"></a>戻り値 - userWidth

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

### <a name="parameters---widthmode"></a>パラメーター - widthMode

値  

### <a name="return-value---widthmode"></a>戻り値 - widthMode

## <a name="method-widthvalue"></a>メソッド widthValue

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a>パラメーター - widthValue

値  

### <a name="return-value---widthvalue"></a>戻り値 - widthValue

## <a name="method-dropex"></a>メソッド dropEx

```xpp
public void dropEx(Array dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---dropex"></a>パラメーター - dropEx

dragSource  

<!-- -->

dragMode  

<!-- -->

x  

<!-- -->

y  

## <a name="method-inputsearch"></a>メソッド inputSearch

```xpp
public void inputSearch(str searchStr)
```

### <a name="parameters---inputsearch"></a>パラメーター - inputSearch

searchStr  

## <a name="method-prefcolumnsize"></a>メソッド prefColumnSize

```xpp
public void prefColumnSize(int width, int height)
```

### <a name="parameters---prefcolumnsize"></a>パラメーター - prefColumnSize

width  

<!-- -->

height  

## <a name="method-gotfocus"></a>メソッド gotFocus

```xpp
public void gotFocus()
```

## <a name="method-lostfocus"></a>メソッド lostFocus

```xpp
public void lostFocus()
```

## <a name="method-mouseleave"></a>メソッド mouseLeave

```xpp
public void mouseLeave()
```

## <a name="method-setfocus"></a>メソッド setFocus

```xpp
public void setFocus()
```

## <a name="method-copy"></a>メソッド copy

```xpp
public void copy()
```

## <a name="method-ongotfocus"></a>メソッド OnGotFocus

```xpp
private void OnGotFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---ongotfocus"></a>パラメーター - OnGotFocus

sender  

<!-- -->

e  

## <a name="method-displaycontrol"></a>メソッド displayControl

```xpp
public void displayControl()
```

## <a name="method-paste"></a>メソッド paste

```xpp
public void paste()
```

## <a name="method-drop"></a>メソッド drop

```xpp
public void drop(FormControl dragSource, FormDrag dragMode, int x, int y)
```

### <a name="parameters---drop"></a>パラメーター - drop

dragSource  

<!-- -->

dragMode  

<!-- -->

x  

<!-- -->

y  

## <a name="method-onlostfocus"></a>メソッド OnLostFocus

```xpp
private void OnLostFocus([FormControl sender], [FormControlEventArgs e])
```

### <a name="parameters---onlostfocus"></a>パラメーター - OnLostFocus

sender  

<!-- -->

e  

## <a name="method-mouseenter"></a>メソッド mouseEnter

```xpp
public void mouseEnter(int x, int y, int button, boolean Ctrl, boolean Shift)
```

### <a name="parameters---mouseenter"></a>パラメーター - mouseEnter

x  

<!-- -->

y  

<!-- -->

ボタン  

<!-- -->

Ctrl  

<!-- -->

Shift  

## <a name="method-resetusersetting"></a>メソッド resetUserSetting

```xpp
public void resetUserSetting()
```

## <a name="method-enddrag"></a>メソッド endDrag

```xpp
public void endDrag()
```

## <a name="method-arrange"></a>メソッド arrange

```xpp
public void arrange()
```

## <a name="method-dragleave"></a>メソッド dragLeave

```xpp
public void dragLeave()
```

## <a name="method-cut"></a>メソッド cut

```xpp
public void cut()
```

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

## <a name="method-context"></a>メソッド context

```xpp
public void context()
```

