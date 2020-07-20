---
title: xClassFactory クラス
description: このトピックでは、xClassFactory クラスについて説明します。
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
ms.openlocfilehash: b4cad1d4937dc48075020448ce02f7a38c6026e9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502766"
---
# <a name="class-xclassfactory"></a>クラス xClassFactory

[!include [banner](../../includes/banner.md)]

```xpp
class xClassFactory extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                               | 説明                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| public xFormRun createAutoReportForm(xArgs args)                                                                                                     |                                                        |
| public xFormRun createLabelForm(xArgs args)                                                                                                          |                                                        |
| public xFormRun createRecInfoForm(xArgs args)                                                                                                        |                                                        |
| public ReportViewer createReportViewer(PrintJobHeader jobsCursor, PrintJobPages pagesCursor, \[ReportRun reportRun\])                                |                                                        |
| public xFormRun createSetupForm(xArgs args)                                                                                                          |                                                        |
| public ReportOutputUser createViewer(PrintJobHeader jobsCursor, PrintJobPages pagesCursor, ReportOutputUserType viewerType, \[ReportRun reportRun\]) |                                                        |
| public Object createWebPageEditor()                                                                                                                  |                                                        |
| public xFormRun formRunClass(xArgs args)                                                                                                             |                                                        |
| public container lastValueGet(SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, \[str design\])               |                                                        |
| public QueryRun queryRunClass(xArgs args)                                                                                                            |                                                        |
| public ReportRun reportRunClass(xArgs args)                                                                                                          |                                                        |
| public Object startAOTWizard(TreeNode parent)                                                                                                        |                                                        |
| public void projectDeleted(str projectName)                                                                                                          |                                                        |
| public void lastValueDelete(SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, \[str design\])                 |                                                        |
| public void lastValuePut(container value, SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, \[str design\])   |                                                        |
| public void drillDown(OutputField outputField, MenuItemType menuItemType, str menuItemName)                                                          |                                                        |
| public void new()                                                                                                                                    | xClassFactory クラスの新しいインスタンスを初期化します。 |

## <a name="method-createautoreportform"></a>メソッド createAutoReportForm

```xpp
public xFormRun createAutoReportForm(xArgs args)
```

### <a name="parameters---createautoreportform"></a>パラメーター - createAutoReportForm

args  

### <a name="return-value---createautoreportform"></a>戻り値 - createAutoReportForm

## <a name="method-createlabelform"></a>メソッド createLabelForm

```xpp
public xFormRun createLabelForm(xArgs args)
```

### <a name="parameters---createlabelform"></a>パラメーター - createLabelForm

args  

### <a name="return-value---createlabelform"></a>戻り値 - createLabelForm

## <a name="method-createrecinfoform"></a>メソッド createRecInfoForm

```xpp
public xFormRun createRecInfoForm(xArgs args)
```

### <a name="parameters---createrecinfoform"></a>パラメーター - createRecInfoForm

args  

### <a name="return-value---createrecinfoform"></a>戻り値 - createRecInfoForm

## <a name="method-createreportviewer"></a>メソッド createReportViewer

```xpp
public ReportViewer createReportViewer(PrintJobHeader jobsCursor, PrintJobPages pagesCursor, [ReportRun reportRun])
```

### <a name="parameters---createreportviewer"></a>パラメーター - createReportViewer

jobsCursor  

<!-- -->

pagesCursor  

<!-- -->

reportRun  

### <a name="return-value---createreportviewer"></a>戻り値 - createReportViewer

## <a name="method-createsetupform"></a>メソッド createSetupForm

```xpp
public xFormRun createSetupForm(xArgs args)
```

### <a name="parameters---createsetupform"></a>パラメーター - createSetupForm

args  

### <a name="return-value---createsetupform"></a>戻り値 - createSetupForm

## <a name="method-createviewer"></a>メソッド createViewer

```xpp
public ReportOutputUser createViewer(PrintJobHeader jobsCursor, PrintJobPages pagesCursor, ReportOutputUserType viewerType, [ReportRun reportRun])
```

### <a name="parameters---createviewer"></a>パラメーター - createViewer

jobsCursor  

<!-- -->

pagesCursor  

<!-- -->

viewerType  

<!-- -->

reportRun  

### <a name="return-value---createviewer"></a>戻り値 - createViewer

## <a name="method-createwebpageeditor"></a>メソッド createWebPageEditor

```xpp
public Object createWebPageEditor()
```

### <a name="return-value---createwebpageeditor"></a>戻り値 - createWebPageEditor

## <a name="method-formrunclass"></a>メソッド formRunClass

```xpp
public xFormRun formRunClass(xArgs args)
```

### <a name="parameters---formrunclass"></a>パラメーター - formRunClass

args  

### <a name="return-value---formrunclass"></a>戻り値 - formRunClass

## <a name="method-lastvalueget"></a>メソッド lastValueGet

```xpp
public container lastValueGet(SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, [str design])
```

### <a name="parameters---lastvalueget"></a>パラメーター - lastValueGet

会社  

<!-- -->

ユーザー  

<!-- -->

utilType  

<!-- -->

名前  

<!-- -->

design  

### <a name="return-value---lastvalueget"></a>戻り値 - lastValueGet

## <a name="method-queryrunclass"></a>メソッド queryRunClass

```xpp
public QueryRun queryRunClass(xArgs args)
```

### <a name="parameters---queryrunclass"></a>パラメーター - queryRunClass

args  

### <a name="return-value---queryrunclass"></a>戻り値 - queryRunClass

## <a name="method-reportrunclass"></a>メソッド reportRunClass

```xpp
public ReportRun reportRunClass(xArgs args)
```

### <a name="parameters---reportrunclass"></a>パラメーター - reportRunClass

args  

### <a name="return-value---reportrunclass"></a>戻り値 - reportRunClass

## <a name="method-startaotwizard"></a>メソッド startAOTWizard

```xpp
public Object startAOTWizard(TreeNode parent)
```

### <a name="parameters---startaotwizard"></a>パラメーター - startAOTWizard

parent  

### <a name="return-value---startaotwizard"></a>戻り値 - startAOTWizard

## <a name="method-projectdeleted"></a>メソッド projectDeleted

```xpp
public void projectDeleted(str projectName)
```

### <a name="parameters---projectdeleted"></a>パラメーター - projectDeleted

projectName  

## <a name="method-lastvaluedelete"></a>メソッド lastValueDelete

```xpp
public void lastValueDelete(SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, [str design])
```

### <a name="parameters---lastvaluedelete"></a>パラメーター - lastValueDelete

会社  

<!-- -->

ユーザー  

<!-- -->

utilType  

<!-- -->

名前  

<!-- -->

design  

## <a name="method-lastvalueput"></a>メソッド lastValuePut

```xpp
public void lastValuePut(container value, SelectableDataArea company, UserId user, UtilElementType utilType, UtilElementName name, [str design])
```

### <a name="parameters---lastvalueput"></a>パラメーター - lastValuePut

値  

<!-- -->

会社  

<!-- -->

ユーザー  

<!-- -->

utilType  

<!-- -->

名前  

<!-- -->

design  

## <a name="method-drilldown"></a>メソッド drillDown

```xpp
public void drillDown(OutputField outputField, MenuItemType menuItemType, str menuItemName)
```

### <a name="parameters---drilldown"></a>パラメーター - drillDown

outputField  

<!-- -->

menuItemType  

<!-- -->

menuItemName  

## <a name="method-new"></a>メソッド new

xClassFactory クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

