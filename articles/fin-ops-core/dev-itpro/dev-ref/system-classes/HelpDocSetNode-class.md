---
title: HelpDocSetNode クラス
description: このトピックでは、HelpDocSetNode クラスについて説明します。
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
ms.openlocfilehash: d9637d35fd5e4cbe88a582bab181a250978f841e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502609"
---
# <a name="class-helpdocsetnode"></a>クラス HelpDocSetNode

[!include [banner](../../includes/banner.md)]

```xpp
class HelpDocSetNode extends TreeNode
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                |
|------------------------------------------------------------|----------------------------------------------------------------------------|
| public boolean addToApplicationHelpMenu(\[boolean value\]) |                                                                            |
| public boolean addToDeveloperHelpMenu(\[boolean value\])   |                                                                            |
| public str changedBy(\[str value\])                        | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。 |
| public Date changedDate(\[Date value\])                    | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。              |
| public str changedTime(\[str value\])                      | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。              |
| public int contentLocation(\[int value\])                  |                                                                            |
| public str createdBy(\[str value\])                        | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。      |
| public Date creationDate(\[Date value\])                   | アプリケーション オブジェクトが作成された日付を取得または設定します。                   |
| public str creationTime(\[str value\])                     |                                                                            |
| public boolean developerDocumentSet(\[boolean value\])     |                                                                            |
| public str documentSetDescription(\[str value\])           |                                                                            |
| public str documentSetName(\[str value\])                  |                                                                            |
| public str helpProviderClass(\[str value\])                |                                                                            |
| public Guid origin(\[Guid value\])                         |                                                                            |
| public boolean userDocumentSet(\[boolean value\])          |                                                                            |
| public void new(str DocSetName)                            | TreeNode クラスの新しいインスタンスを初期化します。                          |

## <a name="method-addtoapplicationhelpmenu"></a>メソッド addToApplicationHelpMenu

```xpp
public boolean addToApplicationHelpMenu([boolean value])
```

### <a name="parameters---addtoapplicationhelpmenu"></a>パラメーター - addToApplicationHelpMenu

値  

### <a name="return-value---addtoapplicationhelpmenu"></a>戻り値 - addToApplicationHelpMenu

## <a name="method-addtodeveloperhelpmenu"></a>メソッド addToDeveloperHelpMenu

```xpp
public boolean addToDeveloperHelpMenu([boolean value])
```

### <a name="parameters---addtodeveloperhelpmenu"></a>パラメーター - addToDeveloperHelpMenu

値  

### <a name="return-value---addtodeveloperhelpmenu"></a>戻り値 - addToDeveloperHelpMenu

## <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a>パラメーター - changedBy

値  

### <a name="return-value---changedby"></a>戻り値 - changedBy

ユーザーの名前。

## <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a>パラメーター - changedDate

値  

### <a name="return-value---changeddate"></a>戻り値 - changedDate

アプリケーション オブジェクトが最後に変更された日付。

## <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a>パラメーター - changedTime

値  

### <a name="return-value---changedtime"></a>戻り値 - changedTime

アプリケーション オブジェクトが最後に変更された時間。

## <a name="method-contentlocation"></a>メソッド contentLocation

```xpp
public int contentLocation([int value])
```

### <a name="parameters---contentlocation"></a>パラメーター - contentLocation

値  

### <a name="return-value---contentlocation"></a>戻り値 - contentLocation

## <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a>パラメーター - createdBy

値  

### <a name="return-value---createdby"></a>戻り値 - createdBy

ユーザーの名前。

## <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a>パラメーター - creationDate

値  

### <a name="return-value---creationdate"></a>戻り値 - creationDate

アプリケーション オブジェクトが作成された日付。

## <a name="method-creationtime"></a>メソッド creationTime

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a>パラメーター - creationTime

値  

### <a name="return-value---creationtime"></a>戻り値 - creationTime

## <a name="method-developerdocumentset"></a>メソッド developerDocumentSet

```xpp
public boolean developerDocumentSet([boolean value])
```

### <a name="parameters---developerdocumentset"></a>パラメーター - developerDocumentSet

値  

### <a name="return-value---developerdocumentset"></a>戻り値 - developerDocumentSet

## <a name="method-documentsetdescription"></a>メソッド documentSetDescription

```xpp
public str documentSetDescription([str value])
```

### <a name="parameters---documentsetdescription"></a>パラメーター - documentSetDescription

値  

### <a name="return-value---documentsetdescription"></a>戻り値 - documentSetDescription

## <a name="method-documentsetname"></a>メソッド documentSetName

```xpp
public str documentSetName([str value])
```

### <a name="parameters---documentsetname"></a>パラメーター - documentSetName

値  

### <a name="return-value---documentsetname"></a>戻り値 - documentSetName

## <a name="method-helpproviderclass"></a>メソッド helpProviderClass

```xpp
public str helpProviderClass([str value])
```

### <a name="parameters---helpproviderclass"></a>パラメーター - helpProviderClass

値  

### <a name="return-value---helpproviderclass"></a>戻り値 - helpProviderClass

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

## <a name="method-userdocumentset"></a>メソッド userDocumentSet

```xpp
public boolean userDocumentSet([boolean value])
```

### <a name="parameters---userdocumentset"></a>パラメーター - userDocumentSet

値  

### <a name="return-value---userdocumentset"></a>戻り値 - userDocumentSet

## <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

```xpp
public void new(str DocSetName)
```

### <a name="parameters---new"></a>パラメーター - new

DocSetName  

