---
title: X++ コンテナー ランタイム関数
description: このトピックでは、コンテナー ランタイム関数について説明します。
author: RobinARH
ms.date: 06/20/2017
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b331a96abfd7143c51a50d13db0770a57b23923a
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783242"
---
# <a name="x-container-runtime-functions"></a>X++ コンテナー ランタイム関数

[!include [banner](../includes/banner.md)]

このトピックでは、コンテナー ランタイム関数について説明します。

これらの関数はコンテナーの内容を操作します。

## <a name="condel"></a>conDel
コンテナーから指定した要素の数を削除します。

### <a name="syntax"></a>構文

```xpp
container conDel(container container, int start, int number)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                 |
|-----------|-------------------------------------------------------------|
| コンテナー | 要素を削除するコンテナー。                      |
| 開始     | 要素の削除を開始する 1 から始まる位置。 |
| 数値    | 削除する要素の数。                           |

### <a name="return-value"></a>戻り値

削除された要素を含まない新しいコンテナーです。

### <a name="example"></a>例

```xpp
static void conDelExample(Args _args)
{
    container c = ["Hello world", 1, 3.14];
        // Deletes the first two items from the container.
        c = conDel(c, 1, 2);
}
```

## <a name="confind"></a>conFind
コンテナー内の最初の要素または一連の要素を検索します。

### <a name="syntax"></a>構文

```xpp
int conFind (container container, anytype element,... )
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                              |
|-----------|----------------------------------------------------------|
| コンテナー | 検索するコンテナー。                                 |
| 要素   | 1 つ以上の要素を検索し、コンマで区切ります。 |

### <a name="remarks"></a>備考

順序で複数の要素を指定する場合は、これらは、コンマで区切られ、正しい順序で指定されている必要があります。 要素は、任意のデータ型にすることができます。

### <a name="return-value"></a>戻り値

**0** 項目が見つからなかった場合。そうでなければ、項目の順序番号。

### <a name="example"></a>例

```xpp
static void conFindExample(Args _args)
{
    container c = ["item1", "item2", "item3"];
    int i;
    int j;
    i = conFind(c, "item2");
    j = conFind(c, "item4");
    print "Position of 'item2' in container is " + int2Str(i);
    print "Position of 'item4' in container is " + int2Str(j);
}
```

## <a name="conins"></a>conIns
コンテナーに 1 つまたは複数の要素を挿入します。

### <a name="syntax"></a>構文

```xpp
container conIns (container container, int start, anytype element, ... )
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                          |
|-----------|------------------------------------------------------|
| コンテナー | 要素を挿入するコンテナー。               |
| 開始     | 要素を挿入する位置。                  |
| 要素   | 1 つ以上の要素を挿入し、コンマで区切ります。 |

### <a name="return-value"></a>戻り値

挿入された要素を含む新しいコンテナーです。

### <a name="remarks"></a>備考

コンテナーの最初の要素は、番号 **1** によって指定されます。. n 番目の要素の後に挿入するには、*開始* パラメーターは n+1 でなければなりません。 また、**+=** 演算子を使用して任意のタイプの値をコンテナに追加することができます。 たとえば、最初の 10 ループ反復処理の自乗値を含むコンテナーを作成するには、次のコードを使用します。

```xpp
int i;
container c;

for (i = 1; i < = 10; i++)
{
    c += i*i;
}
```

### <a name="example"></a>例

```xpp
static void conInsExample(Args _arg)
{
    container c;
    int i;

    c = conIns(c,1,"item1");
    c = conIns(c,2,"item2");
    for (i = 1 ; i <= conLen(c) ; i++)
    {
        // Prints the content of a container.
        print conPeek(c, i);
    }
}
```

## <a name="conlen"></a>conLen
コンテナー内の要素の数を取得します。

### <a name="syntax"></a>構文

```xpp
int conLen(container container)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                       |
|-----------|---------------------------------------------------|
| コンテナー | 要素の数を数えるコンテナー 。 |

### <a name="return-value"></a>戻り値

コンテナー内の要素の数。

### <a name="example"></a>例

```xpp
static void conLenExample(Args _arg)
{
    container c;
    int i;

    c = conins(["item1", "item2"], 1);
    for (i = 1 ; i <= conLen(c) ; i++)
    {
            print conPeek(c, i);
    }
}
```

## <a name="connull"></a>conNull
空のコンテナーを取得します。

```xpp
container conNull()
```

### <a name="remarks"></a>備考

明示的にコンテナーの内容を破棄するには、この機能を使用します。

### <a name="return-value"></a>戻り値

空のコンテナー。

### <a name="example"></a>例

```xpp
static void conNullExample(Args _arg)
{
    container c = ["item1", "item2", "item3"];

    print "Size of container is " + int2str(conLen(c));
    // Set the container to null.
    c = conNull();
    print "Size of container after conNull() is " + int2Str(conLen(c));
}
```

## <a name="conpeek"></a>conPeek
コンテナーから特定の要素を取得し、換算が必要な場合は別のデータ型に変換します。

### <a name="syntax"></a>構文

```xpp
anytype conPeek(container container, int number)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                                                                                                                                                                                      |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| コンテナー | 要素を返すコンテナー。                                                                                                                                                                                         |
| 数値    | 返す要素の位置。 最初の要素を取得するには **1** を指定します。 **-3**、**0** などの無効な位置番号、またはコンテナーの長さより高い番号は予期しないエラーが発生する可能性があります。 |

### <a name="return-value"></a>戻り値

*number* パラメーターで指定された位置にあるコンテナーの要素。 **conPeek** 関数は、参照した項目を予想される戻り値の型に自動的に変換します。 文字列は、整数と実数に自動的に変換され、整数と実数は文字列に変換することができます。

### <a name="example"></a>例

```xpp
static void main(Args _args)
{
    container cnI, cnJ;
    int i, j;
    anytype aty;
    info("container cnI ...");
    cnI = ["itemBlue", "itemYellow"];
    for (i=1; i <= conLen(cnI); i++)
    {
        aty = conPeek(cnI, i);
        info(int2str(i) + " :  " + aty);
    }

    info("container cnJ ...");
    cnJ = conIns(cnI, 2, "ItemInserted");
    for (j=1; j <= conLen(cnJ); j++)
    {
        aty = conPeek(cnJ, j);
        info(int2str(j) + " :  " + aty);
    }
}
/***  Output pasted from InfoLog ...
Message (10:20:03 am)
container cnI ...
1 :  itemBlue
2 :  itemYellow
container cnJ ...
1 :  itemBlue
2 :  ItemInserted
3 :  itemYellow
***/
```

## <a name="conpoke"></a>conPoke
既存の要素を 1 つ以上を置換することでコンテナーを変更します。

### <a name="syntax"></a>構文

```xpp
container conPoke(container container, int start, anytype element, ...)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                           |
|-----------|-------------------------------------------------------|
| コンテナー | 変更するコンテナー。                              |
| 開始     | 置き換える最初の要素の位置。         |
| 要素   | 1 つ以上の要素を置換し、コンマで区切ります。 |

### <a name="return-value"></a>戻り値

新しい要素を含む新しいコンテナーです。

### <a name="remarks"></a>備考

コンテナーの最初の要素は、番号 **1** によって指定されます。.

### <a name="example"></a>例

```xpp
static void conPokeExample(Args _arg)
{
    container c1 = ["item1", "item2", "item3"];
    container c2;
    int i;
    void conPrint(container c)
    {
        for (i = 1 ; i <= conLen(c) ; i++)
        {
            print conPeek(c, i);
        }
    }

    conPrint(c1);
    c2 = conPoke(c1, 2, "PokedItem");
    print "";
    conPrint(c2);
}
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]