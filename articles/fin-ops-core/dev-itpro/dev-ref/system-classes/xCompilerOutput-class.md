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
# <a name="class-xcompileroutput"></a>クラス xCompilerOutput

[!include [banner](../../includes/banner.md)]

```xpp
class xCompilerOutput extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                         | 説明                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| public str getErrorMessage(int errorCode, int severity, str errorString)                                                       |                                                          |
| public container getSquiggleInfo(str treeNodePath)                                                                             |                                                          |
| public void compilerStatus(UtilElementType utilElementType, str utilElementName)                                               |                                                          |
| public void setActiveTab(int tab)                                                                                              |                                                          |
| public void startCompilationObject(str path)                                                                                   |                                                          |
| public void endCompilation()                                                                                                   |                                                          |
| public void startExport()                                                                                                      |                                                          |
| public void startCompilation(int flag, str path, int activeWindowHandle)                                                       |                                                          |
| public void importOutput(str buffer)                                                                                           |                                                          |
| public void endExport()                                                                                                        |                                                          |
| public void endCompilationObject(str path)                                                                                     |                                                          |
| public void startImport()                                                                                                      |                                                          |
| public void new()                                                                                                              | xCompilerOutput クラスの新しいインスタンスを初期化します。 |
| public void compilerOutputMessage(str path, int errorCode, int line, int col, int severity, str errorString, str propertyName) |                                                          |
| public void exportOutput(str buffer)                                                                                           |                                                          |
| public void endCILGenerationOutput()                                                                                           |                                                          |
| public void cilGenerationOutput(str msg, str path, int severity, int line, int col)                                            |                                                          |
| public void endImport()                                                                                                        |                                                          |
| public void nextError()                                                                                                        |                                                          |
| public void startCILGenerationOutput()                                                                                         |                                                          |

## <a name="method-geterrormessage"></a>メソッド getErrorMessage

```xpp
public str getErrorMessage(int errorCode, int severity, str errorString)
```

### <a name="parameters---geterrormessage"></a>パラメーター - getErrorMessage

errorCode  

<!-- -->

severity  

<!-- -->

errorString  

### <a name="return-value---geterrormessage"></a>戻り値 - getErrorMessage

## <a name="method-getsquiggleinfo"></a>メソッド getSquiggleInfo

```xpp
public container getSquiggleInfo(str treeNodePath)
```

### <a name="parameters---getsquiggleinfo"></a>パラメーター - getSquiggleInfo

treeNodePath  

### <a name="return-value---getsquiggleinfo"></a>戻り値 - getSquiggleInfo

## <a name="method-compilerstatus"></a>メソッド compilerStatus

```xpp
public void compilerStatus(UtilElementType utilElementType, str utilElementName)
```

### <a name="parameters---compilerstatus"></a>パラメーター - compilerStatus

utilElementType  

<!-- -->

utilElementName  

## <a name="method-setactivetab"></a>メソッド setActiveTab

```xpp
public void setActiveTab(int tab)
```

### <a name="parameters---setactivetab"></a>パラメーター - setActiveTab

tab  

## <a name="method-startcompilationobject"></a>メソッド startCompilationObject

```xpp
public void startCompilationObject(str path)
```

### <a name="parameters---startcompilationobject"></a>パラメーター - startCompilationObject

path  

## <a name="method-endcompilation"></a>メソッド endCompilation

```xpp
public void endCompilation()
```

## <a name="method-startexport"></a>メソッド startExport

```xpp
public void startExport()
```

## <a name="method-startcompilation"></a>メソッド startCompilation

```xpp
public void startCompilation(int flag, str path, int activeWindowHandle)
```

### <a name="parameters---startcompilation"></a>パラメーター - startCompilation

flag  

<!-- -->

path  

<!-- -->

activeWindowHandle  

## <a name="method-importoutput"></a>メソッド importOutput

```xpp
public void importOutput(str buffer)
```

### <a name="parameters---importoutput"></a>パラメーター - importOutput

バッファ  

## <a name="method-endexport"></a>メソッド endExport

```xpp
public void endExport()
```

## <a name="method-endcompilationobject"></a>メソッド endCompilationObject

```xpp
public void endCompilationObject(str path)
```

### <a name="parameters---endcompilationobject"></a>パラメーター - endCompilationObject

path  

## <a name="method-startimport"></a>メソッド startImport

```xpp
public void startImport()
```

## <a name="method-new"></a>メソッド new

xCompilerOutput クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-compileroutputmessage"></a>メソッド compilerOutputMessage

```xpp
public void compilerOutputMessage(str path, int errorCode, int line, int col, int severity, str errorString, str propertyName)
```

### <a name="parameters---compileroutputmessage"></a>パラメーター - compilerOutputMessage

path  

<!-- -->

errorCode  

<!-- -->

明細行  

<!-- -->

col  

<!-- -->

severity  

<!-- -->

errorString  

<!-- -->

propertyName  

## <a name="method-exportoutput"></a>メソッド exportOutput

```xpp
public void exportOutput(str buffer)
```

### <a name="parameters---exportoutput"></a>パラメーター - exportOutput

バッファ  

## <a name="method-endcilgenerationoutput"></a>メソッド endCILGenerationOutput

```xpp
public void endCILGenerationOutput()
```

## <a name="method-cilgenerationoutput"></a>メソッド cilGenerationOutput

```xpp
public void cilGenerationOutput(str msg, str path, int severity, int line, int col)
```

### <a name="parameters---cilgenerationoutput"></a>パラメーター - cilGenerationOutput

msg  

<!-- -->

path  

<!-- -->

severity  

<!-- -->

明細行  

<!-- -->

col  

## <a name="method-endimport"></a>メソッド endImport

```xpp
public void endImport()
```

## <a name="method-nexterror"></a>メソッド nextError

```xpp
public void nextError()
```

## <a name="method-startcilgenerationoutput"></a>メソッド startCILGenerationOutput

```xpp
public void startCILGenerationOutput()
```

