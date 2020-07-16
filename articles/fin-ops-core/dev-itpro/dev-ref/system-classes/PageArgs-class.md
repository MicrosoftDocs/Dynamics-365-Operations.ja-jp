---
title: PageArgs クラス
description: このトピックでは、PageArgs クラスについて説明します。
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
ms.openlocfilehash: 9b7ddb948842b519de3ca79c9eeaec73db5a59fb
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502539"
---
# <a name="class-pageargs"></a>クラス PageArgs

[!include [banner](../../includes/banner.md)]

```xpp
class PageArgs extends Object
```

PageArgs クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                         | 説明                                                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| public int enumParameter(\[int value\])        | MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。 |
| public int enumTypeParameter(\[int value\])    | MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。                                     |
| public Common externalRecord(\[Common value\]) |                                                                                                             |
| public str menuItemName(\[str value\])         |                                                                                                             |
| public str parameters(\[str value\])           | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。      |
| public void new()                              | PageArgs クラスの新しいインスタンスを初期化します。                                                           |

## <a name="method-enumparameter"></a>メソッド enumParameter

MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティを取得または設定します。

```xpp
public int enumParameter([int value])
```

### <a name="parameters---enumparameter"></a>パラメーター - enumParameter

値  

### <a name="return-value---enumparameter"></a>戻り値 - enumParameter

MenuFunction クラスによって実行されるオブジェクトに渡される enumParameter プロパティ。

## <a name="method-enumtypeparameter"></a>メソッド enumTypeParameter

MenuFunction クラスの enumTypeParameter プロパティを取得または設定します。

```xpp
public int enumTypeParameter([int value])
```

### <a name="parameters---enumtypeparameter"></a>パラメーター - enumTypeParameter

値  

### <a name="return-value---enumtypeparameter"></a>戻り値 - enumTypeParameter

MenuFunction クラスの enumTypeParameter プロパティ。

## <a name="method-externalrecord"></a>メソッド externalRecord

```xpp
public Common externalRecord([Common value])
```

### <a name="parameters---externalrecord"></a>パラメーター - externalRecord

値  

### <a name="return-value---externalrecord"></a>戻り値 - externalRecord

## <a name="method-menuitemname"></a>メソッド menuItemName

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a>パラメーター - menuItemName

値  

### <a name="return-value---menuitemname"></a>戻り値 - menuItemName

## <a name="method-parameters"></a>メソッド parameters

MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。

```xpp
public str parameters([str value])
```

### <a name="parameters---parameters"></a>パラメーター - parameters

値  

### <a name="return-value---parameters"></a>戻り値 - parameters

オブジェクトに渡されるパラメーターのリスト。

### <a name="remarks---parameters"></a>備考 - パラメータ

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 オブジェクトは、渡された未認識のパラメーターを無視します。

## <a name="method-new"></a>メソッド new

PageArgs クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

