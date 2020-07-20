---
title: xFormRun クラス
description: このトピックでは、xFormRun クラスについて説明します。
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
ms.openlocfilehash: 7ce70d3e388e2a1d187b10fe8e22917bb89b9dbd
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502762"
---
# <a name="class-xformrun"></a>クラス xFormRun

[!include [banner](../../includes/banner.md)]

```xpp
class xFormRun extends ObjectRun
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                                                                                                                                                                                         | 説明 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| public boolean allowPrimaryKeyPreview(\[boolean display\])                                                                                                                                                                                                                                                                                                     |             |
| public boolean canClose()                                                                                                                                                                                                                                                                                                                                      |             |
| public boolean canSubmitToWorkflow()                                                                                                                                                                                                                                                                                                                           |             |
| public boolean checkViewOption(int viewOption)                                                                                                                                                                                                                                                                                                                 |             |
| public boolean closed()                                                                                                                                                                                                                                                                                                                                        |             |
| public boolean closedCancel()                                                                                                                                                                                                                                                                                                                                  |             |
| public boolean closedOk()                                                                                                                                                                                                                                                                                                                                      |             |
| public boolean contains(FormControl control)                                                                                                                                                                                                                                                                                                                   |             |
| public FormControl control(int controlId)                                                                                                                                                                                                                                                                                                                      |             |
| public FormControl controlCallingMethod()                                                                                                                                                                                                                                                                                                                      |             |
| public int controlId(str controlName)                                                                                                                                                                                                                                                                                                                          |             |
| public boolean controlMethodOverload(\[boolean value\])                                                                                                                                                                                                                                                                                                        |             |
| public Object controlMethodOverloadObject(\[Object value\])                                                                                                                                                                                                                                                                                                    |             |
| public boolean copy()                                                                                                                                                                                                                                                                                                                                          |             |
| public boolean cut()                                                                                                                                                                                                                                                                                                                                           |             |
| public FormObjectSet dataSource(\[AnyType objectSet\])                                                                                                                                                                                                                                                                                                         |             |
| public int dataSourceCount()                                                                                                                                                                                                                                                                                                                                   |             |
| public FormObjectSet defaultDataSource(\[FormObjectSet value\])                                                                                                                                                                                                                                                                                                |             |
| public boolean defaultInitialQueryValuesOnCreate(\[boolean value\])                                                                                                                                                                                                                                                                                            |             |
| public FormDesign design(\[int reserved\])                                                                                                                                                                                                                                                                                                                     |             |
| public Common docCursor()                                                                                                                                                                                                                                                                                                                                      |             |
| public boolean enableCountryRegion(\[boolean flag\])                                                                                                                                                                                                                                                                                                           |             |
| public Form form()                                                                                                                                                                                                                                                                                                                                             |             |
| public Common getActiveWorkflowConfiguration()                                                                                                                                                                                                                                                                                                                 |             |
| public Common getActiveWorkflowTrackingStatus()                                                                                                                                                                                                                                                                                                                |             |
| public Common getActiveWorkflowWorkItem()                                                                                                                                                                                                                                                                                                                      |             |
| public container getAutoCompleteString(int startIdx, \[FormControl control\], \[str searchString\])                                                                                                                                                                                                                                                            |             |
| public str getFormHelpTopic()                                                                                                                                                                                                                                                                                                                                  |             |
| public FormControl getNextField(FormControl control, \[int flags\])                                                                                                                                                                                                                                                                                            |             |
| public FormControl getPrevField(FormControl control, \[int flags\])                                                                                                                                                                                                                                                                                            |             |
| public boolean hasExecutedInit()                                                                                                                                                                                                                                                                                                                               |             |
| public int hWnd()                                                                                                                                                                                                                                                                                                                                              |             |
| public int installMessageProc(int message, int handle, str method)                                                                                                                                                                                                                                                                                             |             |
| public boolean inViewMode()                                                                                                                                                                                                                                                                                                                                    |             |
| public boolean isDataInteractionSupported()                                                                                                                                                                                                                                                                                                                    |             |
| public boolean isPreloadedInstance()                                                                                                                                                                                                                                                                                                                           |             |
| public boolean isFormPart()                                                                                                                                                                                                                                                                                                                                    |             |
| public boolean isFactBox()                                                                                                                                                                                                                                                                                                                                     |             |
| public boolean isLookupForm()                                                                                                                                                                                                                                                                                                                                  |             |
| public boolean isPartRemote()                                                                                                                                                                                                                                                                                                                                  |             |
| public boolean isPartLocal()                                                                                                                                                                                                                                                                                                                                   |             |
| public boolean isWorkflowEnabled()                                                                                                                                                                                                                                                                                                                             |             |
| public Common loadWorkflowConfiguration()                                                                                                                                                                                                                                                                                                                      |             |
| public boolean lockWindowUpdate(boolean lock)                                                                                                                                                                                                                                                                                                                  |             |
| public str name()                                                                                                                                                                                                                                                                                                                                              |             |
| public FormObjectSet objectSet(\[AnyType objectSet\])                                                                                                                                                                                                                                                                                                          |             |
| public boolean resetAsyncOperationsPendingState()                                                                                                                                                                                                                                                                                                              |             |
| public PageInteraction pageInteraction()                                                                                                                                                                                                                                                                                                                       |             |
| public boolean paste()                                                                                                                                                                                                                                                                                                                                         |             |
| public str recordingScopeId()                                                                                                                                                                                                                                                                                                                                  |             |
| public boolean removeMessageProc(int message, int handle)                                                                                                                                                                                                                                                                                                      |             |
| public List rootFormDataSources()                                                                                                                                                                                                                                                                                                                              |             |
| public boolean selectControl(FormControl control)                                                                                                                                                                                                                                                                                                              |             |
| public FormControl selectedControl()                                                                                                                                                                                                                                                                                                                           |             |
| public Common selectRecordModeSelectedRecord(\[Common selectedRecord\])                                                                                                                                                                                                                                                                                        |             |
| public FormControl selectTarget(\[FormControl target\])                                                                                                                                                                                                                                                                                                        |             |
| public Array tabOrder(\[Array newValue\])                                                                                                                                                                                                                                                                                                                      |             |
| public int task(int taskId)                                                                                                                                                                                                                                                                                                                                    |             |
| public str toString()                                                                                                                                                                                                                                                                                                                                          |             |
| public FormObjectSet workflowDataSource()                                                                                                                                                                                                                                                                                                                      |             |
| public str workflowType()                                                                                                                                                                                                                                                                                                                                      |             |
| public System.Threading.Tasks.Task runAsync(int runAsClassId, str runAsStaticMethodName, container parms, \[System.Threading.CancellationToken cancellationToken\], \[str callbackFormMethodName\], \[container asyncState\], \[str userId\], \[str company\], \[str language\], \[str partitionKey\], \[System.Threading.Tasks.TaskCreationOptions options\]) |             |
| public System.Threading.Tasks.Task setTimeoutEx(\[str formMethodName\], \[container parms\], \[int delay\], \[System.Threading.CancellationToken cancellationToken\])                                                                                                                                                                                          |             |
| public void setParentHandle(int hwnd)                                                                                                                                                                                                                                                                                                                          |             |
| public void setFormHelpTopic(str formHelpTopic)                                                                                                                                                                                                                                                                                                                |             |
| public void setFactBoxEditable()                                                                                                                                                                                                                                                                                                                               |             |
| public void setAutoCompleteString(str string, AnyType control)                                                                                                                                                                                                                                                                                                 |             |
| public void RaiseOnClosing(\[FormEventArgs e\])                                                                                                                                                                                                                                                                                                                |             |
| public void inlineLoadingKey(FormControl parentControl)                                                                                                                                                                                                                                                                                                        |             |
| public void closeSelect(str selectString)                                                                                                                                                                                                                                                                                                                      |             |
| public void RaiseOnActivated(\[FormEventArgs e\])                                                                                                                                                                                                                                                                                                              |             |
| public void prevField(\[int flags\])                                                                                                                                                                                                                                                                                                                           |             |
| public void send()                                                                                                                                                                                                                                                                                                                                             |             |
| public void RaiseOnInitializing(\[FormEventArgs e\])                                                                                                                                                                                                                                                                                                           |             |
| public void updateWorkflowControls()                                                                                                                                                                                                                                                                                                                           |             |
| public void closeCancel()                                                                                                                                                                                                                                                                                                                                      |             |
| public void lastField(\[int flags\])                                                                                                                                                                                                                                                                                                                           |             |
| public void wait(\[boolean modal\])                                                                                                                                                                                                                                                                                                                            |             |
| public void unLock(\[boolean arrangeNow\])                                                                                                                                                                                                                                                                                                                     |             |
| private void OnInitialized(\[xFormRun sender\], \[FormEventArgs e\])                                                                                                                                                                                                                                                                                           |             |
| public void detach()                                                                                                                                                                                                                                                                                                                                           |             |
| public void resetStatusBarBackgroundColor()                                                                                                                                                                                                                                                                                                                    |             |
| private void OnClosing(\[xFormRun sender\], \[FormEventArgs e\])                                                                                                                                                                                                                                                                                               |             |
| public void addDisplayMethod(str name, int displayKind, int displayType, int displayXType, int displayRecord, \[str dataSourceName\], \[boolean isTableDisplayMethod\])                                                                                                                                                                                        |             |
| public void print()                                                                                                                                                                                                                                                                                                                                            |             |
| public void activate(boolean active)                                                                                                                                                                                                                                                                                                                           |             |
| public void resize(int width, int height)                                                                                                                                                                                                                                                                                                                      |             |
| public void reload(\[xArgs args\])                                                                                                                                                                                                                                                                                                                             |             |
| public void finalize()                                                                                                                                                                                                                                                                                                                                         |             |
| public void RaiseOnInitialized(\[FormEventArgs e\])                                                                                                                                                                                                                                                                                                            |             |
| public void resetSize()                                                                                                                                                                                                                                                                                                                                        |             |
| public void clientId(str clientId)                                                                                                                                                                                                                                                                                                                             |             |
| public void createRecord(str formDataSourceName, \[boolean append\])                                                                                                                                                                                                                                                                                           |             |
| public void firstField(\[int flags\])                                                                                                                                                                                                                                                                                                                          |             |
| public void savePersonalization(str controlName, str propertyKey, str propertyValue)                                                                                                                                                                                                                                                                           |             |
| public void expandFactBoxPaneAtStart()                                                                                                                                                                                                                                                                                                                         |             |
| public void redraw()                                                                                                                                                                                                                                                                                                                                           |             |
| public void arrange()                                                                                                                                                                                                                                                                                                                                          |             |
| public void blockPersonalization(boolean blockPersonalization)                                                                                                                                                                                                                                                                                                 |             |
| public void nextField(\[int flags\])                                                                                                                                                                                                                                                                                                                           |             |
| public void nextGroup()                                                                                                                                                                                                                                                                                                                                        |             |
| public void prevGroup()                                                                                                                                                                                                                                                                                                                                        |             |
| public void setFormPartStyle(boolean isFactBox)                                                                                                                                                                                                                                                                                                                |             |
| public void run()                                                                                                                                                                                                                                                                                                                                              |             |
| public void setActive()                                                                                                                                                                                                                                                                                                                                        |             |
| public void closeSelectRecord(Common selectedRecord)                                                                                                                                                                                                                                                                                                           |             |
| public void registerFormSpecializedCustomControl(str customControlName)                                                                                                                                                                                                                                                                                        |             |
| public void setApply(Object object, \[Object parm\])                                                                                                                                                                                                                                                                                                           |             |
| public void new(xArgs args)                                                                                                                                                                                                                                                                                                                                    |             |
| public void RegisterXppILImplementation(str className)                                                                                                                                                                                                                                                                                                         |             |
| public void sysColorChanged()                                                                                                                                                                                                                                                                                                                                  |             |
| public void selectRecordMode(\[FormControl control\])                                                                                                                                                                                                                                                                                                          |             |
| private void OnPostRun(\[xFormRun sender\], \[FormEventArgs e\])                                                                                                                                                                                                                                                                                               |             |
| public void skipSaveUserSetting(boolean skip)                                                                                                                                                                                                                                                                                                                  |             |
| public void selectMode(\[FormControl control\])                                                                                                                                                                                                                                                                                                                |             |
| public void printPreview()                                                                                                                                                                                                                                                                                                                                     |             |
| private void OnActivated(\[xFormRun sender\], \[FormEventArgs e\])                                                                                                                                                                                                                                                                                             |             |
| public void collapseFactBoxPaneAtStart()                                                                                                                                                                                                                                                                                                                       |             |
| public void lock()                                                                                                                                                                                                                                                                                                                                             |             |
| public void init()                                                                                                                                                                                                                                                                                                                                             |             |
| public void formOnTop()                                                                                                                                                                                                                                                                                                                                        |             |
| public void close()                                                                                                                                                                                                                                                                                                                                            |             |
| public void delAutoCompleteString(\[AnyType control\])                                                                                                                                                                                                                                                                                                         |             |
| public void closeOk()                                                                                                                                                                                                                                                                                                                                          |             |
| public void modeledQueryName(str queryName)                                                                                                                                                                                                                                                                                                                    |             |
| public void initWorkflowControls()                                                                                                                                                                                                                                                                                                                             |             |
| public void setOrder(FormControl control, FormControl control1, \[boolean before\])                                                                                                                                                                                                                                                                            |             |
| public void allowCrossFormLinks(boolean allowCrossFormLinks)                                                                                                                                                                                                                                                                                                   |             |
| public void RaiseOnPostRun(\[FormEventArgs e\])                                                                                                                                                                                                                                                                                                                |             |
| public void setStatusBarBackgroundColor(int a, int r, int g, int b)                                                                                                                                                                                                                                                                                            |             |
| public void loadPersonalization()                                                                                                                                                                                                                                                                                                                              |             |
| public void doApply()                                                                                                                                                                                                                                                                                                                                          |             |
| private void OnInitializing(\[xFormRun sender\], \[FormEventArgs e\])                                                                                                                                                                                                                                                                                          |             |
| public void flushCountryRegionCodeCache()                                                                                                                                                                                                                                                                                                                      |             |
| public void localRefresh()                                                                                                                                                                                                                                                                                                                                     |             |

## <a name="method-allowprimarykeypreview"></a>メソッド allowPrimaryKeyPreview

```xpp
public boolean allowPrimaryKeyPreview([boolean display])
```

### <a name="parameters---allowprimarykeypreview"></a>パラメーター - allowPrimaryKeyPreview

表示  

### <a name="return-value---allowprimarykeypreview"></a>戻り値 - allowPrimaryKeyPreview

## <a name="method-canclose"></a>メソッド canClose

```xpp
public boolean canClose()
```

### <a name="return-value---canclose"></a>戻り値 - canClose

## <a name="method-cansubmittoworkflow"></a>メソッド canSubmitToWorkflow

```xpp
public boolean canSubmitToWorkflow()
```

### <a name="return-value---cansubmittoworkflow"></a>戻り値 - canSubmitToWorkflow

## <a name="method-checkviewoption"></a>メソッド checkViewOption

```xpp
public boolean checkViewOption(int viewOption)
```

### <a name="parameters---checkviewoption"></a>パラメーター - checkViewOption

viewOption  

### <a name="return-value---checkviewoption"></a>戻り値 - checkViewOption

## <a name="method-closed"></a>メソッド closed

```xpp
public boolean closed()
```

### <a name="return-value---closed"></a>戻り値 - closed

## <a name="method-closedcancel"></a>メソッド closedCancel

```xpp
public boolean closedCancel()
```

### <a name="return-value---closedcancel"></a>戻り値 - closedCancel

## <a name="method-closedok"></a>メソッド closedOk

```xpp
public boolean closedOk()
```

### <a name="return-value---closedok"></a>戻り値 - closedOk

## <a name="method-contains"></a>メソッド contains

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a>パラメーター - contains

control  

### <a name="return-value---contains"></a>戻り値 - contains

## <a name="method-control"></a>メソッド control

```xpp
public FormControl control(int controlId)
```

### <a name="parameters---control"></a>パラメーター - control

controlId  

### <a name="return-value---control"></a>戻り値 - control

## <a name="method-controlcallingmethod"></a>メソッド controlCallingMethod

```xpp
public FormControl controlCallingMethod()
```

### <a name="return-value---controlcallingmethod"></a>戻り値 - controlCallingMethod

## <a name="method-controlid"></a>メソッド controlId

```xpp
public int controlId(str controlName)
```

### <a name="parameters---controlid"></a>パラメーター - controlId

controlName  

### <a name="return-value---controlid"></a>戻り値 - controlId

## <a name="method-controlmethodoverload"></a>メソッド controlMethodOverload

```xpp
public boolean controlMethodOverload([boolean value])
```

### <a name="parameters---controlmethodoverload"></a>パラメーター - controlMethodOverload

値  

### <a name="return-value---controlmethodoverload"></a>戻り値 - controlMethodOverload

## <a name="method-controlmethodoverloadobject"></a>メソッド controlMethodOverloadObject

```xpp
public Object controlMethodOverloadObject([Object value])
```

### <a name="parameters---controlmethodoverloadobject"></a>パラメーター - controlMethodOverloadObject

値  

### <a name="return-value---controlmethodoverloadobject"></a>戻り値 - controlMethodOverloadObject

## <a name="method-copy"></a>メソッド copy

```xpp
public boolean copy()
```

### <a name="return-value---copy"></a>戻り値 - copy

## <a name="method-cut"></a>メソッド cut

```xpp
public boolean cut()
```

### <a name="return-value---cut"></a>戻り値 - cut

## <a name="method-datasource"></a>メソッド dataSource

```xpp
public FormObjectSet dataSource([AnyType objectSet])
```

### <a name="parameters---datasource"></a>パラメーター - dataSource

objectSet  

### <a name="return-value---datasource"></a>戻り値 - dataSource

## <a name="method-datasourcecount"></a>メソッド dataSourceCount

```xpp
public int dataSourceCount()
```

### <a name="return-value---datasourcecount"></a>戻り値 - dataSourceCount

## <a name="method-defaultdatasource"></a>メソッド defaultDataSource

```xpp
public FormObjectSet defaultDataSource([FormObjectSet value])
```

### <a name="parameters---defaultdatasource"></a>パラメーター - defaultDataSource

値  

### <a name="return-value---defaultdatasource"></a>戻り値 - defaultDataSource

## <a name="method-defaultinitialqueryvaluesoncreate"></a>メソッド defaultInitialQueryValuesOnCreate

```xpp
public boolean defaultInitialQueryValuesOnCreate([boolean value])
```

### <a name="parameters---defaultinitialqueryvaluesoncreate"></a>パラメーター - defaultInitialQueryValuesOnCreate

値  

### <a name="return-value---defaultinitialqueryvaluesoncreate"></a>戻り値 - defaultInitialQueryValuesOnCreate

## <a name="method-design"></a>メソッド design

```xpp
public FormDesign design([int reserved])
```

### <a name="parameters---design"></a>パラメーター - design

reserved  

### <a name="return-value---design"></a>戻り値 - design

## <a name="method-doccursor"></a>メソッド docCursor

```xpp
public Common docCursor()
```

### <a name="return-value---doccursor"></a>戻り値 - docCursor

## <a name="method-enablecountryregion"></a>メソッド enableCountryRegion

```xpp
public boolean enableCountryRegion([boolean flag])
```

### <a name="parameters---enablecountryregion"></a>パラメーター - enableCountryRegion

flag  

### <a name="return-value---enablecountryregion"></a>戻り値 - enableCountryRegion

## <a name="method-form"></a>メソッド form

```xpp
public Form form()
```

### <a name="return-value---form"></a>戻り値 - form

## <a name="method-getactiveworkflowconfiguration"></a>メソッド getActiveWorkflowConfiguration

```xpp
public Common getActiveWorkflowConfiguration()
```

### <a name="return-value---getactiveworkflowconfiguration"></a>戻り値 - getActiveWorkflowConfiguration

## <a name="method-getactiveworkflowtrackingstatus"></a>メソッド getActiveWorkflowTrackingStatus

```xpp
public Common getActiveWorkflowTrackingStatus()
```

### <a name="return-value---getactiveworkflowtrackingstatus"></a>戻り値 - getActiveWorkflowTrackingStatus

## <a name="method-getactiveworkflowworkitem"></a>メソッド getActiveWorkflowWorkItem

```xpp
public Common getActiveWorkflowWorkItem()
```

### <a name="return-value---getactiveworkflowworkitem"></a>戻り値 - getActiveWorkflowWorkItem

## <a name="method-getautocompletestring"></a>メソッド getAutoCompleteString

```xpp
public container getAutoCompleteString(int startIdx, [FormControl control], [str searchString])
```

### <a name="parameters---getautocompletestring"></a>パラメーター - getAutoCompleteString

startIdx  

<!-- -->

control  

<!-- -->

searchString  

### <a name="return-value---getautocompletestring"></a>戻り値 - getAutoCompleteString

## <a name="method-getformhelptopic"></a>メソッド getFormHelpTopic

```xpp
public str getFormHelpTopic()
```

### <a name="return-value---getformhelptopic"></a>戻り値 - getFormHelpTopic

## <a name="method-getnextfield"></a>メソッド getNextField

```xpp
public FormControl getNextField(FormControl control, [int flags])
```

### <a name="parameters---getnextfield"></a>パラメーター - getNextField

control  

<!-- -->

flags  

### <a name="return-value---getnextfield"></a>戻り値 - getNextField

## <a name="method-getprevfield"></a>メソッド getPrevField

```xpp
public FormControl getPrevField(FormControl control, [int flags])
```

### <a name="parameters---getprevfield"></a>パラメーター - getPrevField

control  

<!-- -->

flags  

### <a name="return-value---getprevfield"></a>戻り値 - getPrevField

## <a name="method-hasexecutedinit"></a>メソッド hasExecutedInit

```xpp
public boolean hasExecutedInit()
```

### <a name="return-value---hasexecutedinit"></a>戻り値 - hasExecutedInit

## <a name="method-hwnd"></a>メソッド hWnd

```xpp
public int hWnd()
```

### <a name="return-value---hwnd"></a>戻り値 - hWnd

## <a name="method-installmessageproc"></a>メソッド installMessageProc

```xpp
public int installMessageProc(int message, int handle, str method)
```

### <a name="parameters---installmessageproc"></a>パラメーター - installMessageProc

メッセージ  

<!-- -->

handle  

<!-- -->

メソッド  

### <a name="return-value---installmessageproc"></a>戻り値 - installMessageProc

## <a name="method-inviewmode"></a>メソッド inViewMode

```xpp
public boolean inViewMode()
```

### <a name="return-value---inviewmode"></a>戻り値 - inViewMode

## <a name="method-isdatainteractionsupported"></a>メソッド isDataInteractionSupported

```xpp
public boolean isDataInteractionSupported()
```

### <a name="return-value---isdatainteractionsupported"></a>戻り値 - isDataInteractionSupported

## <a name="method-ispreloadedinstance"></a>メソッド isPreloadedInstance

```xpp
public boolean isPreloadedInstance()
```

### <a name="return-value---ispreloadedinstance"></a>戻り値 - isPreloadedInstance

## <a name="method-isformpart"></a>メソッド isFormPart

```xpp
public boolean isFormPart()
```

### <a name="return-value---isformpart"></a>戻り値 - isFormPart

## <a name="method-isfactbox"></a>メソッド isFactBox

```xpp
public boolean isFactBox()
```

### <a name="return-value---isfactbox"></a>戻り値 - isFactBox

## <a name="method-islookupform"></a>メソッド isLookupForm

```xpp
public boolean isLookupForm()
```

### <a name="return-value---islookupform"></a>戻り値 - isLookupForm

## <a name="method-ispartremote"></a>メソッド isPartRemote

```xpp
public boolean isPartRemote()
```

### <a name="return-value---ispartremote"></a>戻り値 - isPartRemote

## <a name="method-ispartlocal"></a>メソッド isPartLocal

```xpp
public boolean isPartLocal()
```

### <a name="return-value---ispartlocal"></a>戻り値 - isPartLocal

## <a name="method-isworkflowenabled"></a>メソッド isWorkflowEnabled

```xpp
public boolean isWorkflowEnabled()
```

### <a name="return-value---isworkflowenabled"></a>戻り値 - isWorkflowEnabled

## <a name="method-loadworkflowconfiguration"></a>メソッド loadWorkflowConfiguration

```xpp
public Common loadWorkflowConfiguration()
```

### <a name="return-value---loadworkflowconfiguration"></a>戻り値 - loadWorkflowConfiguration

## <a name="method-lockwindowupdate"></a>メソッド lockWindowUpdate

```xpp
public boolean lockWindowUpdate(boolean lock)
```

### <a name="parameters---lockwindowupdate"></a>パラメーター - lockWindowUpdate

lock  

### <a name="return-value---lockwindowupdate"></a>戻り値 - lockWindowUpdate

## <a name="method-name"></a>メソッド名

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

## <a name="method-objectset"></a>メソッド objectSet

```xpp
public FormObjectSet objectSet([AnyType objectSet])
```

### <a name="parameters---objectset"></a>パラメーター - objectSet

objectSet  

### <a name="return-value---objectset"></a>戻り値 - objectSet

## <a name="method-resetasyncoperationspendingstate"></a>メソッド resetAsyncOperationsPendingState

```xpp
public boolean resetAsyncOperationsPendingState()
```

### <a name="return-value---resetasyncoperationspendingstate"></a>戻り値 - resetAsyncOperationsPendingState

## <a name="method-pageinteraction"></a>メソッド pageInteraction

```xpp
public PageInteraction pageInteraction()
```

### <a name="return-value---pageinteraction"></a>戻り値 - pageInteraction

## <a name="method-paste"></a>メソッド paste

```xpp
public boolean paste()
```

### <a name="return-value---paste"></a>戻り値 - paste

## <a name="method-recordingscopeid"></a>メソッド recordingScopeId

```xpp
public str recordingScopeId()
```

### <a name="return-value---recordingscopeid"></a>戻り値 - recordingScopeId

## <a name="method-removemessageproc"></a>メソッド removeMessageProc

```xpp
public boolean removeMessageProc(int message, int handle)
```

### <a name="parameters---removemessageproc"></a>パラメーター - removeMessageProc

メッセージ  

<!-- -->

handle  

### <a name="return-value---removemessageproc"></a>戻り値 - removeMessageProc

## <a name="method-rootformdatasources"></a>メソッド rootFormDataSources

```xpp
public List rootFormDataSources()
```

### <a name="return-value---rootformdatasources"></a>戻り値 - rootFormDataSources

## <a name="method-selectcontrol"></a>メソッド selectControl

```xpp
public boolean selectControl(FormControl control)
```

### <a name="parameters---selectcontrol"></a>パラメーター - selectControl

control  

### <a name="return-value---selectcontrol"></a>戻り値 - selectControl

## <a name="method-selectedcontrol"></a>メソッド selectedControl

```xpp
public FormControl selectedControl()
```

### <a name="return-value---selectedcontrol"></a>戻り値 - selectedControl

## <a name="method-selectrecordmodeselectedrecord"></a>メソッド selectRecordModeSelectedRecord

```xpp
public Common selectRecordModeSelectedRecord([Common selectedRecord])
```

### <a name="parameters---selectrecordmodeselectedrecord"></a>パラメーター - selectRecordModeSelectedRecord

selectedRecord  

### <a name="return-value---selectrecordmodeselectedrecord"></a>戻り値 - selectRecordModeSelectedRecord

## <a name="method-selecttarget"></a>メソッド selectTarget

```xpp
public FormControl selectTarget([FormControl target])
```

### <a name="parameters---selecttarget"></a>パラメーター - selectTarget

target  

### <a name="return-value---selecttarget"></a>戻り値 - selectTarget

## <a name="method-taborder"></a>メソッド tabOrder

```xpp
public Array tabOrder([Array newValue])
```

### <a name="parameters---taborder"></a>パラメーター - tabOrder

newValue  

### <a name="return-value---taborder"></a>戻り値 - tabOrder

## <a name="method-task"></a>メソッド task

```xpp
public int task(int taskId)
```

### <a name="parameters---task"></a>パラメーター - task

taskId  

### <a name="return-value---task"></a>戻り値 - task

## <a name="method-tostring"></a>メソッド toString

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

## <a name="method-workflowdatasource"></a>メソッド workflowDataSource

```xpp
public FormObjectSet workflowDataSource()
```

### <a name="return-value---workflowdatasource"></a>戻り値 - workflowDataSource

## <a name="method-workflowtype"></a>メソッド workflowType

```xpp
public str workflowType()
```

### <a name="return-value---workflowtype"></a>戻り値 - workflowType

## <a name="method-runasync"></a>メソッド runAsync

```xpp
public System.Threading.Tasks.Task runAsync(int runAsClassId, str runAsStaticMethodName, container parms, [System.Threading.CancellationToken cancellationToken], [str callbackFormMethodName], [container asyncState], [str userId], [str company], [str language], [str partitionKey], [System.Threading.Tasks.TaskCreationOptions options])
```

### <a name="parameters---runasync"></a>パラメーター - runAsync

runAsClassId  

<!-- -->

runAsStaticMethodName  

<!-- -->

parms  

<!-- -->

cancellationToken  

<!-- -->

callbackFormMethodName  

<!-- -->

asyncState  

<!-- -->

userId  

<!-- -->

会社  

<!-- -->

言語  

<!-- -->

partitionKey  

<!-- -->

オプション  

### <a name="return-value---runasync"></a>戻り値 - runAsync

## <a name="method-settimeoutex"></a>メソッド setTimeoutEx

```xpp
public System.Threading.Tasks.Task setTimeoutEx([str formMethodName], [container parms], [int delay], [System.Threading.CancellationToken cancellationToken])
```

### <a name="parameters---settimeoutex"></a>パラメーター - setTimeoutEx

formMethodName  

<!-- -->

parms  

<!-- -->

遅延  

<!-- -->

cancellationToken  

### <a name="return-value---settimeoutex"></a>戻り値 - setTimeoutEx

## <a name="method-setparenthandle"></a>メソッド setParentHandle

```xpp
public void setParentHandle(int hwnd)
```

### <a name="parameters---setparenthandle"></a>パラメーター - setParentHandle

hwnd  

## <a name="method-setformhelptopic"></a>メソッド setFormHelpTopic

```xpp
public void setFormHelpTopic(str formHelpTopic)
```

### <a name="parameters---setformhelptopic"></a>パラメーター - setFormHelpTopic

formHelpTopic  

## <a name="method-setfactboxeditable"></a>メソッド setFactBoxEditable

```xpp
public void setFactBoxEditable()
```

## <a name="method-setautocompletestring"></a>メソッド setAutoCompleteString

```xpp
public void setAutoCompleteString(str string, AnyType control)
```

### <a name="parameters---setautocompletestring"></a>パラメーター - setAutoCompleteString

文字列  

<!-- -->

control  

## <a name="method-raiseonclosing"></a>メソッド RaiseOnClosing

```xpp
public void RaiseOnClosing([FormEventArgs e])
```

### <a name="parameters---raiseonclosing"></a>パラメーター - RaiseOnClosing

e  

## <a name="method-inlineloadingkey"></a>メソッド inlineLoadingKey

```xpp
public void inlineLoadingKey(FormControl parentControl)
```

### <a name="parameters---inlineloadingkey"></a>パラメータ－ - inlineLoadingKey

parentControl  

## <a name="method-closeselect"></a>メソッド closeSelect

```xpp
public void closeSelect(str selectString)
```

### <a name="parameters---closeselect"></a>パラメーター - closeSelect

selectString  

## <a name="method-raiseonactivated"></a>メソッド RaiseOnActivated

```xpp
public void RaiseOnActivated([FormEventArgs e])
```

### <a name="parameters---raiseonactivated"></a>パラメーター - RaiseOnActivated

e  

## <a name="method-prevfield"></a>メソッド prevField

```xpp
public void prevField([int flags])
```

### <a name="parameters---prevfield"></a>パラメーター - prevField

flags  

## <a name="method-send"></a>メソッド send

```xpp
public void send()
```

## <a name="method-raiseoninitializing"></a>メソッド RaiseOnInitializing

```xpp
public void RaiseOnInitializing([FormEventArgs e])
```

### <a name="parameters---raiseoninitializing"></a>パラメーター - RaiseOnInitializing

e  

## <a name="method-updateworkflowcontrols"></a>メソッド updateWorkflowControls

```xpp
public void updateWorkflowControls()
```

## <a name="method-closecancel"></a>メソッド closeCancel

```xpp
public void closeCancel()
```

## <a name="method-lastfield"></a>メソッド lastField

```xpp
public void lastField([int flags])
```

### <a name="parameters---lastfield"></a>パラメーター - lastField

flags  

## <a name="method-wait"></a>メソッド wait

```xpp
public void wait([boolean modal])
```

### <a name="parameters---wait"></a>パラメーター - wait

modal  

## <a name="method-unlock"></a>メソッド unLock

```xpp
public void unLock([boolean arrangeNow])
```

### <a name="parameters---unlock"></a>パラメーター - unLock

arrangeNow  

## <a name="method-oninitialized"></a>メソッド OnInitialized

```xpp
private void OnInitialized([xFormRun sender], [FormEventArgs e])
```

### <a name="parameters---oninitialized"></a>パラメーター - OnInitialized

sender  

<!-- -->

e  

## <a name="method-detach"></a>メソッド detach

```xpp
public void detach()
```

## <a name="method-resetstatusbarbackgroundcolor"></a>メソッド resetStatusBarBackgroundColor

```xpp
public void resetStatusBarBackgroundColor()
```

## <a name="method-onclosing"></a>メソッド OnClosing

```xpp
private void OnClosing([xFormRun sender], [FormEventArgs e])
```

### <a name="parameters---onclosing"></a>パラメーター - OnClosing

sender  

<!-- -->

e  

## <a name="method-adddisplaymethod"></a>メソッド addDisplayMethod

```xpp
public void addDisplayMethod(str name, int displayKind, int displayType, int displayXType, int displayRecord, [str dataSourceName], [boolean isTableDisplayMethod])
```

### <a name="parameters---adddisplaymethod"></a>パラメーター - addDisplayMethod

名前  

<!-- -->

displayKind  

<!-- -->

displayType  

<!-- -->

displayXType  

<!-- -->

displayRecord  

<!-- -->

dataSourceName  

<!-- -->

isTableDisplayMethod  

## <a name="method-print"></a>メソッド print

```xpp
public void print()
```

## <a name="method-activate"></a>メソッド activate

```xpp
public void activate(boolean active)
```

### <a name="parameters---activate"></a>パラメーター - activate

有効  

## <a name="method-resize"></a>メソッド resize

```xpp
public void resize(int width, int height)
```

### <a name="parameters---resize"></a>パラメーター - resize

width  

<!-- -->

height  

## <a name="method-reload"></a>メソッド reload

```xpp
public void reload([xArgs args])
```

### <a name="parameters---reload"></a>パラメーター - reload

args  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-raiseoninitialized"></a>メソッド RaiseOnInitialized

```xpp
public void RaiseOnInitialized([FormEventArgs e])
```

### <a name="parameters---raiseoninitialized"></a>パラメーター - RaiseOnInitialized

e  

## <a name="method-resetsize"></a>メソッド resetSize

```xpp
public void resetSize()
```

## <a name="method-clientid"></a>メソッド clientId

```xpp
public void clientId(str clientId)
```

### <a name="parameters---clientid"></a>パラメーター - clientId

clientId  

## <a name="method-createrecord"></a>メソッド createRecord

```xpp
public void createRecord(str formDataSourceName, [boolean append])
```

### <a name="parameters---createrecord"></a>パラメーター - createRecord

formDataSourceName  

<!-- -->

append  

## <a name="method-firstfield"></a>メソッド firstField

```xpp
public void firstField([int flags])
```

### <a name="parameters---firstfield"></a>パラメーター - firstField

flags  

## <a name="method-savepersonalization"></a>メソッド savePersonalization

```xpp
public void savePersonalization(str controlName, str propertyKey, str propertyValue)
```

### <a name="parameters---savepersonalization"></a>パラメーター - savePersonalization

controlName  

<!-- -->

propertyKey  

<!-- -->

propertyValue  

## <a name="method-expandfactboxpaneatstart"></a>メソッド expandFactBoxPaneAtStart

```xpp
public void expandFactBoxPaneAtStart()
```

## <a name="method-redraw"></a>メソッド redraw

```xpp
public void redraw()
```

## <a name="method-arrange"></a>メソッド arrange

```xpp
public void arrange()
```

## <a name="method-blockpersonalization"></a>メソッド blockPersonalization

```xpp
public void blockPersonalization(boolean blockPersonalization)
```

### <a name="parameters---blockpersonalization"></a>パラメーター - blockPersonalization

blockPersonalization  

## <a name="method-nextfield"></a>メソッド nextField

```xpp
public void nextField([int flags])
```

### <a name="parameters---nextfield"></a>パラメーター - nextField

flags  

## <a name="method-nextgroup"></a>メソッド nextGroup

```xpp
public void nextGroup()
```

## <a name="method-prevgroup"></a>メソッド prevGroup

```xpp
public void prevGroup()
```

## <a name="method-setformpartstyle"></a>メソッド setFormPartStyle

```xpp
public void setFormPartStyle(boolean isFactBox)
```

### <a name="parameters---setformpartstyle"></a>パラメーター - setFormPartStyle

isFactBox  

## <a name="method-run"></a>メソッド run

```xpp
public void run()
```

## <a name="method-setactive"></a>メソッド setActive

```xpp
public void setActive()
```

## <a name="method-closeselectrecord"></a>メソッド closeSelectRecord

```xpp
public void closeSelectRecord(Common selectedRecord)
```

### <a name="parameters---closeselectrecord"></a>パラメーター - closeSelectRecord

selectedRecord  

## <a name="method-registerformspecializedcustomcontrol"></a>メソッド registerFormSpecializedCustomControl

```xpp
public void registerFormSpecializedCustomControl(str customControlName)
```

### <a name="parameters---registerformspecializedcustomcontrol"></a>パラメーター - registerFormSpecializedCustomControl

customControlName  

## <a name="method-setapply"></a>メソッド setApply

```xpp
public void setApply(Object object, [Object parm])
```

### <a name="parameters---setapply"></a>パラメーター - setApply

オブジェクト  

<!-- -->

parm  

## <a name="method-new"></a>メソッド new

```xpp
public void new(xArgs args)
```

### <a name="parameters---new"></a>パラメーター - new

args  

## <a name="method-registerxppilimplementation"></a>メソッド RegisterXppILImplementation

```xpp
public void RegisterXppILImplementation(str className)
```

### <a name="parameters---registerxppilimplementation"></a>パラメーター - RegisterXppILImplementation

className  

## <a name="method-syscolorchanged"></a>メソッド sysColorChanged

```xpp
public void sysColorChanged()
```

## <a name="method-selectrecordmode"></a>メソッド selectRecordMode

```xpp
public void selectRecordMode([FormControl control])
```

### <a name="parameters---selectrecordmode"></a>パラメーター - selectRecordMode

control  

## <a name="method-onpostrun"></a>メソッド OnPostRun

```xpp
private void OnPostRun([xFormRun sender], [FormEventArgs e])
```

### <a name="parameters---onpostrun"></a>パラメーター - OnPostRun

sender  

<!-- -->

e  

## <a name="method-skipsaveusersetting"></a>メソッド skipSaveUserSetting

```xpp
public void skipSaveUserSetting(boolean skip)
```

### <a name="parameters---skipsaveusersetting"></a>パラメーター - skipSaveUserSetting

skip  

## <a name="method-selectmode"></a>メソッド selectMode

```xpp
public void selectMode([FormControl control])
```

### <a name="parameters---selectmode"></a>パラメーター - selectMode

control  

## <a name="method-printpreview"></a>メソッド printPreview

```xpp
public void printPreview()
```

## <a name="method-onactivated"></a>メソッド OnActivated

```xpp
private void OnActivated([xFormRun sender], [FormEventArgs e])
```

### <a name="parameters---onactivated"></a>パラメーター - OnActivated

sender  

<!-- -->

e  

## <a name="method-collapsefactboxpaneatstart"></a>メソッド collapseFactBoxPaneAtStart

```xpp
public void collapseFactBoxPaneAtStart()
```

## <a name="method-lock"></a>メソッド lock

```xpp
public void lock()
```

## <a name="method-init"></a>メソッド init

```xpp
public void init()
```

## <a name="method-formontop"></a>メソッド formOnTop

```xpp
public void formOnTop()
```

## <a name="method-close"></a>メソッド close

```xpp
public void close()
```

## <a name="method-delautocompletestring"></a>メソッド delAutoCompleteString

```xpp
public void delAutoCompleteString([AnyType control])
```

### <a name="parameters---delautocompletestring"></a>パラメーター - delAutoCompleteString

control  

## <a name="method-closeok"></a>メソッド closeOk

```xpp
public void closeOk()
```

## <a name="method-modeledqueryname"></a>メソッド modeledQueryName

```xpp
public void modeledQueryName(str queryName)
```

### <a name="parameters---modeledqueryname"></a>パラメーター - modeledQueryName

queryName  

## <a name="method-initworkflowcontrols"></a>メソッド initWorkflowControls

```xpp
public void initWorkflowControls()
```

## <a name="method-setorder"></a>メソッド setOrder

```xpp
public void setOrder(FormControl control, FormControl control1, [boolean before])
```

### <a name="parameters---setorder"></a>パラメーター - setOrder

control  

<!-- -->

control1  

<!-- -->

以前  

## <a name="method-allowcrossformlinks"></a>メソッド allowCrossFormLinks

```xpp
public void allowCrossFormLinks(boolean allowCrossFormLinks)
```

### <a name="parameters---allowcrossformlinks"></a>パラメーター - allowCrossFormLinks

allowCrossFormLinks  

## <a name="method-raiseonpostrun"></a>メソッド RaiseOnPostRun

```xpp
public void RaiseOnPostRun([FormEventArgs e])
```

### <a name="parameters---raiseonpostrun"></a>パラメーター - RaiseOnPostRun

e  

## <a name="method-setstatusbarbackgroundcolor"></a>メソッド setStatusBarBackgroundColor

```xpp
public void setStatusBarBackgroundColor(int a, int r, int g, int b)
```

### <a name="parameters---setstatusbarbackgroundcolor"></a>パラメーター - setStatusBarBackgroundColor

a  

<!-- -->

r  

<!-- -->

g  

<!-- -->

b  

## <a name="method-loadpersonalization"></a>メソッド loadPersonalization

```xpp
public void loadPersonalization()
```

## <a name="method-doapply"></a>メソッド doApply

```xpp
public void doApply()
```

## <a name="method-oninitializing"></a>メソッド OnInitializing

```xpp
private void OnInitializing([xFormRun sender], [FormEventArgs e])
```

### <a name="parameters---oninitializing"></a>パラメーター - OnInitializing

sender  

<!-- -->

e  

## <a name="method-flushcountryregioncodecache"></a>メソッド flushCountryRegionCodeCache

```xpp
public void flushCountryRegionCodeCache()
```

## <a name="method-localrefresh"></a>メソッド localRefresh

```xpp
public void localRefresh()
```

