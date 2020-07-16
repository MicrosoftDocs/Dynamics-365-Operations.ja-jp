---
title: xResourceNode クラス
description: このトピックでは、xResourceNode クラスについて説明します。
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
ms.openlocfilehash: d1faadc69bdfe0b635b48751e43425450b8e227f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502759"
---
# <a name="class-xresourcenode"></a>クラス xResourceNode

[!include [banner](../../includes/banner.md)]

```xpp
class xResourceNode extends TreeNode
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                   | 説明 |
|--------------------------------------------------------------------------|-------------|
| public BinData AOTGetData()                                              |             |
| public Image AOTGetImage()                                               |             |
| public str changedBy(\[str value\])                                      |             |
| public Date changedDate(\[Date value\])                                  |             |
| public str changedTime(\[str value\])                                    |             |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\]) |             |
| public str createdBy(\[str value\])                                      |             |
| public Date creationDate(\[Date value\])                                 |             |
| public str creationTime(\[str value\])                                   |             |
| public str filename(\[str value\])                                       |             |
| public str helpText(\[str value\])                                       |             |
| public str label(\[str value\])                                          |             |
| public str name(\[str value\])                                           |             |
| public Guid origin(\[Guid value\])                                       |             |
| ::public static Image AOTCreateImage(str imageName)                      |             |
| public void AOTSetData(BinData data)                                     |             |
| public void AOTSetImage(Image image)                                     |             |

## <a name="method-aotgetdata"></a>メソッド AOTGetData

```xpp
public BinData AOTGetData()
```

### <a name="return-value---aotgetdata"></a>戻り値 - AOTGetData

## <a name="method-aotgetimage"></a>メソッド AOTGetImage

```xpp
public Image AOTGetImage()
```

### <a name="return-value---aotgetimage"></a>戻り値 - AOTGetImage

## <a name="method-changedby"></a>メソッド changedBy

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a>パラメーター - changedBy

値  

### <a name="return-value---changedby"></a>戻り値 - changedBy

## <a name="method-changeddate"></a>メソッド changedDate

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a>パラメーター - changedDate

値  

### <a name="return-value---changeddate"></a>戻り値 - changedDate

## <a name="method-changedtime"></a>メソッド changedTime

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a>パラメーター - changedTime

値  

### <a name="return-value---changedtime"></a>戻り値 - changedTime

## <a name="method-configurationkey"></a>メソッド configurationKey

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a>パラメーター - configurationKey

値  

### <a name="return-value---configurationkey"></a>戻り値 - configurationKey

## <a name="method-createdby"></a>メソッド createdBy

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a>パラメーター - createdBy

値  

### <a name="return-value---createdby"></a>戻り値 - createdBy

## <a name="method-creationdate"></a>メソッド creationDate

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a>パラメーター - creationDate

値  

### <a name="return-value---creationdate"></a>戻り値 - creationDate

## <a name="method-creationtime"></a>メソッド creationTime

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a>パラメーター - creationTime

値  

### <a name="return-value---creationtime"></a>戻り値 - creationTime

## <a name="method-filename"></a>メソッド filename

```xpp
public str filename([str value])
```

### <a name="parameters---filename"></a>パラメーター - filename

値  

### <a name="return-value---filename"></a>戻り値 - filename

## <a name="method-helptext"></a>メソッド helpText

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a>パラメーター - helpText

値  

### <a name="return-value---helptext"></a>戻り値 - helpText

## <a name="method-label"></a>メソッド label

```xpp
public str label([str value])
```

### <a name="parameters---label"></a>パラメーター - label

値  

### <a name="return-value---label"></a>戻り値 - label

## <a name="method-name"></a>メソッド名

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  

### <a name="return-value---name"></a>戻り値 - name

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

## <a name="method-aotcreateimage"></a>メソッド AOTCreateImage

```xpp
public static Image AOTCreateImage(str imageName)
```

### <a name="parameters---aotcreateimage"></a>パラメーター - AOTCreateImage

imageName  

### <a name="return-value---aotcreateimage"></a>戻り値 - AOTCreateImage

## <a name="method-aotsetdata"></a>メソッド AOTSetData

```xpp
public void AOTSetData(BinData data)
```

### <a name="parameters---aotsetdata"></a>パラメーター - AOTSetData

データ  

## <a name="method-aotsetimage"></a>メソッド AOTSetImage

```xpp
public void AOTSetImage(Image image)
```

### <a name="parameters---aotsetimage"></a>パラメーター - AOTSetImage

画像  

