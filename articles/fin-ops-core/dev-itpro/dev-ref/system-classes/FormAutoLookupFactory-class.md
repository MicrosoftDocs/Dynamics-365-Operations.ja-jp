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
# <a name="class-formautolookupfactory"></a>クラス FormAutoLookupFactory

[!include [banner](../../includes/banner.md)]

```xpp
class FormAutoLookupFactory extends FieldBinding
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                              | 説明                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| ::public static xFormRun buildLookupFormByField (FormControl controlHostingLookup, FieldBinding fieldBinding)                                                                        |                                                                |
| ::public static xFormRun buildLookupFromCustomForm (FormControl controlHostingLookup, Form customLookupForm, FieldBinding fieldBinding, \[xArgs customArgs\], \[Query customQuery\]) |                                                                |
| ::public static xFormRun buildReferenceLookupFromCustomForm (FormReferenceControl referenceControlHostingLookup, Form customLookupForm, \[xArgs customArgs\], \[Query customQuery\]) |                                                                |
| ::public static void createLookupForClientsideControl (xFormRun parentForm, str targetId, str controlName, int tableId, int fieldId, str controlValue, boolean isInFilterMode)       |                                                                |
| ::public static void performFormLookup(xFormRun lookupForm, \[boolean blockUntilLookupClosed\], \[FormControl controlHostingLookup\])                                               |                                                                |
| private void new()                                                                                                                                                                  | FormAutoLookupFactory クラスの新しいインスタンスを初期化します。 |

## <a name="method-buildlookupformbyfield"></a>メソッド buildLookupFormByField

```xpp
public static xFormRun buildLookupFormByField(FormControl controlHostingLookup, FieldBinding fieldBinding)
```

### <a name="parameters---buildlookupformbyfield"></a>パラメーター - buildLookupFormByField

controlHostingLookup  

<!-- -->

fieldBinding  

### <a name="return-value---buildlookupformbyfield"></a>戻り値 - buildLookupFormByField

## <a name="method-buildlookupfromcustomform"></a>メソッド buildLookupFromCustomForm

```xpp
public static xFormRun buildLookupFromCustomForm(FormControl controlHostingLookup, Form customLookupForm, FieldBinding fieldBinding, [xArgs customArgs], [Query customQuery])
```

### <a name="parameters---buildlookupfromcustomform"></a>パラメーター - buildLookupFromCustomForm

controlHostingLookup  

<!-- -->

customLookupForm  

<!-- -->

fieldBinding  

<!-- -->

customArgs  

<!-- -->

customQuery  

### <a name="return-value---buildlookupfromcustomform"></a>戻り値 - buildLookupFromCustomForm

## <a name="method-buildreferencelookupfromcustomform"></a>メソッド buildReferenceLookupFromCustomForm

```xpp
public static xFormRun buildReferenceLookupFromCustomForm(FormReferenceControl referenceControlHostingLookup, Form customLookupForm, [xArgs customArgs], [Query customQuery])
```

### <a name="parameters---buildreferencelookupfromcustomform"></a>パラメーター - buildReferenceLookupFromCustomForm

referenceControlHostingLookup  

<!-- -->

customLookupForm  

<!-- -->

customArgs  

<!-- -->

customQuery  

### <a name="return-value---buildreferencelookupfromcustomform"></a>戻り値 - buildReferenceLookupFromCustomForm

## <a name="method-createlookupforclientsidecontrol"></a>メソッド createLookupForClientsideControl

```xpp
public static void createLookupForClientsideControl(xFormRun parentForm, str targetId, str controlName, int tableId, int fieldId, str controlValue, boolean isInFilterMode)
```

### <a name="parameters---createlookupforclientsidecontrol"></a>パラメーター - createLookupForClientsideControl

parentForm  

<!-- -->

targetId  

<!-- -->

controlName  

<!-- -->

tableId  

<!-- -->

fieldId  

<!-- -->

controlValue  

<!-- -->

isInFilterMode  

## <a name="method-performformlookup"></a>メソッド performFormLookup

```xpp
public static void performFormLookup(xFormRun lookupForm, [boolean blockUntilLookupClosed], [FormControl controlHostingLookup])
```

### <a name="parameters---performformlookup"></a>パラメーター - performFormLookup

lookupForm  

<!-- -->

blockUntilLookupClosed  

<!-- -->

controlHostingLookup  

## <a name="method-new"></a>メソッド new

FormAutoLookupFactory クラスの新しいインスタンスを初期化します。

```xpp
private void new()
```

