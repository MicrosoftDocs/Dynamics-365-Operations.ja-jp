---
title: FormReferenceObject クラス
description: このトピックでは、FormReferenceObject クラスについて説明します。
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
ms.openlocfilehash: 881776dd66f2531741d2e73152cfb02a343b16c6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502622"
---
# <a name="class-formreferenceobject"></a>クラス FormReferenceObject

[!include [banner](../../includes/banner.md)]

```xpp
class FormReferenceObject extends FormDataObject
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                    | 説明                                                                                                                                                             |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public int allowAdd(\[int value\])                                        | フォーム データ オブジェクトの allowAdd プロパティの値を設定するか返します。                                                                                            |
| public boolean allowEdit(\[boolean value\])                               | ユーザーがコントロールの内容を変更できるかどうかを示します。                                                                                                      |
| public FieldId dataField(\[FieldId value\])                               |                                                                                                                                                                         |
| public boolean enabled(\[boolean value\])                                 | オブジェクトを有効または無効にするかどうかを示します。                                                                                                                      |
| public Common lookupReference(FormReferenceControl formReferenceControl)  |                                                                                                                                                                         |
| public boolean mandatory(\[boolean value\])                               | データ フィールドが必須であるかどうかを示す値を設定するか返します。                                                                                             |
| public Common resolveReference(FormReferenceControl formReferenceControl) |                                                                                                                                                                         |
| public boolean skip(\[boolean value\])                                    | ユーザーが Tab キーを押して、データ ソースに関連付けられたコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。 |
| public boolean visible(\[boolean value\])                                 | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |

## <a name="method-allowadd"></a>メソッド allowAdd

フォーム データ オブジェクトの allowAdd プロパティの値を設定するか返します。

```xpp
public int allowAdd([int value])
```

### <a name="parameters---allowadd"></a>パラメーター - allowAdd

値  
allowEdit プロパティに割り当てられている値。

### <a name="return-value---allowadd"></a>戻り値 - allowAdd

allowAdd プロパティが No、Restricted もしくは Yes に設定されているかどうかを示す FormAllowAdd 列挙値。

## <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを示します。

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a>パラメーター - allowEdit

値  

### <a name="return-value---allowedit"></a>戻り値 - allowEdit

コントロールを編集することができる場合は true。それ以外の場合は、false。

### <a name="remarks---allowedit"></a>備考 - allowEdit

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

## <a name="method-datafield"></a>メソッド dataField

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a>パラメーター - dataField

値  

### <a name="return-value---datafield"></a>戻り値 - dataField

## <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを示します。

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a>パラメーター - enabled

値  

### <a name="return-value---enabled"></a>戻り値 - enabled

オブジェクトが有効である場合は true。それ以外の場合は、false。

### <a name="remarks---enabled"></a>備考 - enabled

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

## <a name="method-lookupreference"></a>メソッド lookupReference

```xpp
public Common lookupReference(FormReferenceControl formReferenceControl)
```

### <a name="parameters---lookupreference"></a>パラメーター - lookupReference

formReferenceControl  

### <a name="return-value---lookupreference"></a>戻り値 - lookupReference

## <a name="method-mandatory"></a>メソッド mandatory

データ フィールドが必須であるかどうかを示す値を設定するか返します。

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a>パラメーター - mandatory

値  
フィールドの必須プロパティに割り当てられる値。

### <a name="return-value---mandatory"></a>戻り値 - mandatory

フィールドが必須項目である場合は true。それ以外の場合は、false。

## <a name="method-resolvereference"></a>メソッド resolveReference

```xpp
public Common resolveReference(FormReferenceControl formReferenceControl)
```

### <a name="parameters---resolvereference"></a>パラメーター - resolveReference

formReferenceControl  

### <a name="return-value---resolvereference"></a>戻り値 - resolveReference

## <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押して、データ ソースに関連付けられたコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a>パラメーター - skip

値  
コントロールに関連付けられているデータ ソースの skip プロパティに割り当てられている値 (オプション)。

### <a name="return-value---skip"></a>戻り値 - skip

データ ソースに関連付けられているコントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="remarks---skip"></a>備考 - skip

有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。 コントロールまたはデータ ソースのスキップ値が true の場合、コントロールはスキップされます。

## <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a>パラメーター - visible

値  
コントロールの表示設定に割り当てられている値。

### <a name="return-value---visible"></a>戻り値 - visible

コントロールが可視である場合は true。それ以外の場合は false。 既定は true です。

### <a name="remarks---visible"></a>備考 - visible

データ ソース フィールドを参照するコントロールは、コントロールおよび基になるデータ ソース フィールドの両方で Visible プロパティが true に設定されている場合にのみ表示されます。 コントロールの代わりにデータ ソース フィールドのプロパティを設定することにより、フォーム全体で一貫してフィールドが処理されることを確認します。 これにより、アップグレードが容易になります。

