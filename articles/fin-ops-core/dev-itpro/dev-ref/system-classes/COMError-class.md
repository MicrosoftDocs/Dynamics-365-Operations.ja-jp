---
title: COMError クラス
description: このトピックでは、COMError クラスについて説明します。
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
ms.openlocfilehash: 79fc9e6ed9ae32546964a1b22b664d631a4b7c91
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502713"
---
# <a name="class-comerror"></a>クラス COMError

[!include [banner](../../includes/banner.md)]

```xpp
class COMError extends Object
```

COMError クラスは、COM メソッド呼び出し時に発生するすべての COM エラーをラップします。

## <a name="remarks"></a>備考

COM メソッド呼び出し中にエラーが発生すると、エラー コードとエラーの説明が COMError オブジェクトに格納されます。 COM クラスに関連付けられている COMError オブジェクトは、COM.error メソッドを使用して COM クラスから取得されます。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                   | 説明                                                                                                               |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------|
| public str description() | COM オブジェクトが呼び出されたときに発生したエラーの説明を返します。                                          |
| public int helpContext() | COM オブジェクトが呼び出されたときに発生したエラーのヘルプ コンテキスト ID を返します。                                   |
| public str helpFile()    | COM オブジェクトが呼び出されたときに発生したエラーに関する情報が含まれるヘルプ ファイルの名前を返します。 |
| public int number()      | COM オブジェクトが呼び出されたときに発生したエラーのエラー コードを返します。                                         |
| public str source()      | COM オブジェクトが呼び出されたときに発生したエラーを引き起こしたコンポーネントの名前を返します。                     |
| public str toString()    | クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。                           |
| public void clear()      | COMError オブジェクトのプロパティをクリアします。                                                                             |
| public void new()        | COMError クラスのインスタンスを初期化します。                                                                            |
| public void finalize()   |                                                                                                                           |

## <a name="method-description"></a>メソッドの説明

COM オブジェクトが呼び出されたときに発生したエラーの説明を返します。

```xpp
public str description()
```

### <a name="return-value---description"></a>戻り値 - description

エラーの説明です。

### <a name="remarks---description"></a>備考 - description

COM オブジェクトがテキストのエラー メッセージの手渡しをサポートしていない場合は、説明が空白になることがあります。 説明のプロパティは読み取り専用です。

## <a name="method-helpcontext"></a>メソッド helpContext

COM オブジェクトが呼び出されたときに発生したエラーのヘルプ コンテキスト ID を返します。

```xpp
public int helpContext()
```

### <a name="return-value---helpcontext"></a>戻り値 - helpContext

ヘルプ コンテキスト ID。

### <a name="remarks---helpcontext"></a>備考 - helpContext

ヘルプ コンテキスト ID は、COM オブジェクトがエラーのヘルプをサポートしていない場合、0 (ゼロ) にすることができます。 helpContext プロパティは読み取り専用です。

## <a name="method-helpfile"></a>メソッド helpFile

COM オブジェクトが呼び出されたときに発生したエラーに関する情報が含まれるヘルプ ファイルの名前を返します。

```xpp
public str helpFile()
```

### <a name="return-value---helpfile"></a>戻り値 - helpFile

ヘルプ ファイルの名前。

### <a name="remarks---helpfile"></a>備考 - helpFile

ヘルプ ファイルは、COM オブジェクトがエラーのヘルプをサポートしていない場合、空にすることができます。 helpFile プロパティは読み取り専用です。

## <a name="method-number"></a>メソッド number

COM オブジェクトが呼び出されたときに発生したエラーのエラー コードを返します。

```xpp
public int number()
```

### <a name="return-value---number"></a>戻り値 - number

エラーコード。COM オブジェクトが呼び出されたときにエラーが発生しなかった場合は 0 (ゼロ)。

### <a name="remarks---number"></a>備考 - number

数プロパティは読み取り専用です。

## <a name="method-source"></a>メソッド source

COM オブジェクトが呼び出されたときに発生したエラーを引き起こしたコンポーネントの名前を返します。

```xpp
public str source()
```

### <a name="return-value---source"></a>戻り値 - source

エラーのソース。

### <a name="remarks---source"></a>備考 - source

COM オブジェクトがエラーのソースの手渡しをサポートしていない場合は、ソースが空白になることがあります。 ソースのプロパティは読み取り専用です。

## <a name="method-tostring"></a>メソッド toString

クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

クラスのテキストの説明。

### <a name="remarks---tostring"></a>備考 - toString

ほとんどのクラスでは、返される文字列には、クラス ハンドルと名前が含まれています。 ただし、一部のクラスでは、文字列に追加情報が追加されます。

## <a name="method-clear"></a>メソッド clear

COMError オブジェクトのプロパティをクリアします。

```xpp
public void clear()
```

### <a name="remarks---clear"></a>備考 - clear

通常、COMError オブジェクトのプロパティは読み取り専用ですが、このメソッドを使用して解除できます。

## <a name="method-new"></a>メソッド new

COMError クラスのインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

