---
title: XppPrePostArgs クラス
description: このトピックでは、XppPrePostArgs クラスについて説明します。
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
ms.openlocfilehash: c374813b5c3e1d9890e3751c048f90398572f5d8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502774"
---
# <a name="class-xppprepostargs"></a>クラス XppPrePostArgs

[!include [banner](../../includes/banner.md)]

```xpp
class XppPrePostArgs extends XppEventArgs
```

XppPrePostArgs クラスは、プリハンドラーとポストハンドラーのためのパブリッシャーの引数と戻り値に関する情報を提供します。

## <a name="remarks"></a>備考

パブリッシャーは、プリイベントとポストイベントを公開するメソッドです。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                       | 説明                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| public boolean wrapper(str fieldName, AnyType value)                                         |                                                                                                             |
| public struct args()                                                                         |                                                                                                             |
| public boolean existsArg(str fieldName)                                                      | 出版社の引数の存在を名前でチェックします。                                                   |
| public AnyType getArgNum(int argIndex)                                                       | パブリッシャーの引数をインデックスごとに取得します。                                                               |
| public int setArgNum(int argIndex, AnyType value)                                            | パブリッシャーの引数をインデックスごとに設定します。                                                                     |
| public AnyType value(str fieldName)                                                          |                                                                                                             |
| public XppEventHandlerCalledWhen getCalledWhen()                                             | プリハンドラーまたはポストハンドラーをインスタンスが現在提供しているかどうかを示す値を取得します。 |
| public AnyType getReturnValue()                                                              | 発行元の戻り値を取得します。                                                                          |
| public AnyType getThis()                                                                     | 発行元の「this」参照を取得します。                                                                      |
| public boolean removeArg(str fieldName)                                                      |                                                                                                             |
| public int wrapper(str fieldName, AnyType value)                                             |                                                                                                             |
| public int setReturnValue(AnyType retval)                                                    | 発行元の戻り値を設定します。                                                                          |
| public str isFirst()                                                                         |                                                                                                             |
| public void setCalledWhen(XppEventHandlerCalledWhen calledWhen)                              | プリハンドラーまたはポストハンドラーをインスタンスが現在提供しているかどうかを設定します。                             |
| ::public static void setReturnValueEx(AnyType retval, XppPrePostArgs args)                   |                                                                                                             |
| public void new(\[AnyType thisPtr\], \[str args\], \[XppEventHandlerCalledWhen calledWhen\]) | Object クラスの新しいインスタンスを初期化します。                                                             |

## <a name="method-wrapper"></a>メソッド wrapper

```xpp
public boolean wrapper(str fieldName, AnyType value)
```

### <a name="parameters---wrapper"></a>パラメーター - wrapper

fieldName  

<!-- -->

値  

### <a name="return-value---wrapper"></a>戻り値 - wrapper

## <a name="method-args"></a>メソッド args

```xpp
public struct args()
```

### <a name="return-value---args"></a>戻り値 - args

## <a name="method-existsarg"></a>メソッド existsArg

出版社の引数の存在を名前でチェックします。

```xpp
public boolean existsArg(str fieldName)
```

### <a name="parameters---existsarg"></a>パラメーター - existsArg

fieldName  

### <a name="return-value---existsarg"></a>戻り値 - existsArg

指定された引数が存在するかどうかを示すブール値データ型。

### <a name="remarks---existsarg"></a>備考 - existsArg

引数名は大文字と小文字を区別しません。

## <a name="method-getargnum"></a>メソッド getArgNum

パブリッシャーの引数をインデックスごとに取得します。

```xpp
public AnyType getArgNum(int argIndex)
```

### <a name="parameters---getargnum"></a>パラメーター - getArgNum

argIndex  
ターゲット引数の int インデックス。

### <a name="return-value---getargnum"></a>戻り値 - getArgNum

指定された引数の anytype 値です。

### <a name="remarks---getargnum"></a>備考 - getArgNum

インデックスの範囲は、静的パブリッシャーの場合は 0 ベース、インスタンス パブリッシャーの場合は 1 ベースです。

## <a name="method-setargnum"></a>メソッド setArgNum

パブリッシャーの引数をインデックスごとに設定します。

```xpp
public int setArgNum(int argIndex, AnyType value)
```

### <a name="parameters---setargnum"></a>パラメーター - setArgNum

argIndex  
指定された引数に割り当てる anytype 値です。

<!-- -->

値  
指定された引数に割り当てる anytype 値です。

### <a name="return-value---setargnum"></a>戻り値 - setArgNum

int データ型値 1 。

### <a name="remarks---setargnum"></a>備考 - setArgNum

インデックスの範囲は、静的パブリッシャーの場合は 0 ベース、インスタンス パブリッシャーの場合は 1 ベースです。

## <a name="method-value"></a>メソッド value

```xpp
public AnyType value(str fieldName)
```

### <a name="parameters---value"></a>パラメーター - value

fieldName  

### <a name="return-value---value"></a>戻り値 - value

## <a name="method-getcalledwhen"></a>メソッド getCalledWhen

プリハンドラーまたはポストハンドラーをインスタンスが現在提供しているかどうかを示す値を取得します。

```xpp
public XppEventHandlerCalledWhen getCalledWhen()
```

### <a name="return-value---getcalledwhen"></a>戻り値 - getCalledWhen

XppPrePostArgs インスタンスはプリハンドラーまたはポストハンドラーかどうかを示す XppEventHandlerCalledWhen データ型値です。

## <a name="method-getreturnvalue"></a>メソッド getReturnValue

発行元の戻り値を取得します。

```xpp
public AnyType getReturnValue()
```

### <a name="return-value---getreturnvalue"></a>戻り値 - getReturnValue

anytype データ型値は、発行元の戻り値を表します。

### <a name="remarks---getreturnvalue"></a>備考 - getReturnValue

このメソッドは、プリハンドラー用ではありません。

## <a name="method-getthis"></a>メソッド getThis

発行元の「this」参照を取得します。

```xpp
public AnyType getThis()
```

### <a name="return-value---getthis"></a>戻り値 - getThis

anytype データ型値は、発行元の「this」参照を表します。

### <a name="remarks---getthis"></a>備考 - getThis

パブリッシャーが静的な場合は、nullNothingnullptrunita null 参照 (Visual Basic ではなしになる) を返します。

## <a name="method-removearg"></a>メソッド removeArg

```xpp
public boolean removeArg(str fieldName)
```

### <a name="parameters---removearg"></a>パラメーター - removeArg

fieldName  

### <a name="return-value---removearg"></a>戻り値 - removeArg

## <a name="method-wrapper"></a>メソッド wrapper

```xpp
public int wrapper(str fieldName, AnyType value)
```

### <a name="parameters---wrapper"></a>パラメーター - wrapper

fieldName  

<!-- -->

値  

### <a name="return-value---wrapper"></a>戻り値 - wrapper

## <a name="method-setreturnvalue"></a>メソッド setReturnValue

発行元の戻り値を設定します。

```xpp
public int setReturnValue(AnyType retval)
```

### <a name="parameters---setreturnvalue"></a>パラメーター - setReturnValue

retval  

### <a name="return-value---setreturnvalue"></a>戻り値 - setReturnValue

int データ型値 1 。

### <a name="remarks---setreturnvalue"></a>備考 - setReturnValue

このメソッドは、プリハンドラーまたは無効を返すパブリッシャーのためのものではありません。

## <a name="method-isfirst"></a>メソッド isFirst

```xpp
public str isFirst()
```

### <a name="return-value---isfirst"></a>戻り値 - isFirst

## <a name="method-setcalledwhen"></a>メソッド setCalledWhen

プリハンドラーまたはポストハンドラーをインスタンスが現在提供しているかどうかを設定します。

```xpp
public void setCalledWhen(XppEventHandlerCalledWhen calledWhen)
```

### <a name="parameters---setcalledwhen"></a>パラメーター - setCalledWhen

calledWhen  

### <a name="remarks---setcalledwhen"></a>備考 - setCalledWhen

このメソッドは、プリハンドラーまたはポストハンドラーのコードから明示的に呼び出されてはなりません。 このメソッドは、単体テストおよび自動生成コード用に予約されています。

## <a name="method-setreturnvalueex"></a>メソッド setReturnValueEx

```xpp
public static void setReturnValueEx(AnyType retval, XppPrePostArgs args)
```

### <a name="parameters---setreturnvalueex"></a>パラメーター - setReturnValueEx

retval  

<!-- -->

args  

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new([AnyType thisPtr], [str args], [XppEventHandlerCalledWhen calledWhen])
```

### <a name="parameters---new"></a>パラメーター - new

thisPtr  

<!-- -->

args  

<!-- -->

calledWhen  

