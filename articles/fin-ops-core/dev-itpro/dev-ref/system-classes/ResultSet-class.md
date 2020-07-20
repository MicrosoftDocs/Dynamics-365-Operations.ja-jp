---
title: ResultSet クラス
description: このトピックでは、ResultSet クラスについて説明します。
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
ms.openlocfilehash: bc53d9eaa15cf239178f06ca142fa64c8a9effed
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502823"
---
# <a name="class-resultset"></a>クラス ResultSet

[!include [banner](../../includes/banner.md)]

```xpp
class ResultSet extends Object
```

ResultSet クラスは、ステートメントを実行することによって生成されるデータ テーブルへのアクセス許可を提供します。

## <a name="remarks"></a>備考

最大可搬性については、各行内の ResultSet 列は左から右の順に読み込まれ、各列は 1 回だけ読み込まれる必要があります。 ResultSet は、インスタンスを実行することによって生成されるデータ テーブルへのアクセス許可を提供します。 テーブル行は順番に取得されます。 行内の列の値は任意の順序でアクセスすることができます。 ResultSet は、現在のデータ行を指すカーソルを保持します。 最初、カーソルは最初の行の前に配置されます。 "next" メソッドは、次の行にカーソルを移動します。 getXX メソッドについては、アプリケーションは基になるデータを指定したタイプに変換し、適切な値を返そうとします。 getXX メソッドは、現在の行の列の値を取得します。 列のインデックス番号を使用して値を取得します。 列は、連番が 1 から振られます。 ResultSet は、そのステートメントがクローズ、再実行、または複数の結果のシーケンスから次の結果を取得されるために使用されるときに、ResultSet を作成したステートメントによって自動的に終了されます。

## <a name="examples"></a>例

```xpp
static void example() 
{ 
    Connection Con; 
    Statement Stmt; 
    ResultSet R; 
    SqlStatementExecutePermission perm; 
    str sql = 'SELECT VALUE FROM SQLSYSTEMVARIABLES'; 
    Con = new Connection(); 
    Stmt = Con.createStatement(); 
    perm = new SqlStatementExecutePermission(sql); 
    perm.assert(); 
    R = Stmt.executeQuery(sql); 
    while ( R.next() ) 
    { 
        print R.getString(1); 
    } 
}
```

## <a name="methods"></a>メソッド

| 方法                                    | 説明                                                                               |
|-------------------------------------------|-------------------------------------------------------------------------------------------|
| public boolean getBoolean(int ColumnID)   | 現在の行で列のブール値を取得します。                               |
| public int getByte(int ColumnID)          |                                                                                           |
| public Date getDate(int ColumnID)         | 現在の行で列のブール値を日付値として取得します。 |
| public DateTime getDateTime(int ColumnID) |                                                                                           |
| public Guid getGuid(int ColumnID)         |                                                                                           |
| public int getInt(int ColumnID)           | 現在の行で列のブール値を整数として取得します。                         |
| public Int64 getInt64(int ColumnID)       |                                                                                           |
| public ResultSetMetaData getMetaData()    |                                                                                           |
| public Real getReal(int ColumnID)         | タイプ実数の値として現在の行の列の値を取得します。           |
| public str getString(int ColumnID)        | 現在の行で列の文字列値を取得します。                                     |
| public boolean next()                     | 1 番目またはそれ以降の行を選択します。                                                      |
| public boolean wasNull(int ColumnID)      | 最後の列の読み取りが SQL NULL 値を持つかどうかを報告します。                              |
| public void close()                       | オブジェクトのデータベースのリソースをすぐに解放します。                                     |

## <a name="method-getboolean"></a>メソッド getBoolean

現在の行で列のブール値を取得します。

```xpp
public boolean getBoolean(int ColumnID)
```

### <a name="parameters---getboolean"></a>パラメーター - getBoolean

ColumnID  
列 ID。

### <a name="return-value---getboolean"></a>戻り値 - getBoolean

現在の行で列の値。

## <a name="method-getbyte"></a>メソッド getByte

```xpp
public int getByte(int ColumnID)
```

### <a name="parameters---getbyte"></a>パラメーター - getByte

ColumnID  

### <a name="return-value---getbyte"></a>戻り値 - getByte

## <a name="method-getdate"></a>メソッド getDate

現在の行で列のブール値を日付値として取得します。

```xpp
public Date getDate(int ColumnID)
```

### <a name="parameters---getdate"></a>パラメーター - getDate

ColumnID  
列の ID。

### <a name="return-value---getdate"></a>戻り値 - getDate

日付。

## <a name="method-getdatetime"></a>メソッド getDateTime

```xpp
public DateTime getDateTime(int ColumnID)
```

### <a name="parameters---getdatetime"></a>パラメーター - getDateTime

ColumnID  

### <a name="return-value---getdatetime"></a>戻り値 - getDateTime

## <a name="method-getguid"></a>メソッド getGuid

```xpp
public Guid getGuid(int ColumnID)
```

### <a name="parameters---getguid"></a>パラメーター - getGuid

ColumnID  

### <a name="return-value---getguid"></a>戻り値 - getGuid

## <a name="method-getint"></a>メソッド getInt

現在の行で列のブール値を整数として取得します。

```xpp
public int getInt(int ColumnID)
```

### <a name="parameters---getint"></a>パラメーター - getInt

ColumnID  
列 ID。

### <a name="return-value---getint"></a>戻り値 - getInt

列の整数値。

## <a name="method-getint64"></a>メソッド getInt64

```xpp
public Int64 getInt64(int ColumnID)
```

### <a name="parameters---getint64"></a>パラメーター - getInt64

ColumnID  

### <a name="return-value---getint64"></a>戻り値 - getInt64

## <a name="method-getmetadata"></a>メソッド getMetaData

```xpp
public ResultSetMetaData getMetaData()
```

### <a name="return-value---getmetadata"></a>戻り値 - getMetaData

## <a name="method-getreal"></a>メソッド getReal

タイプ実数の値として現在の行の列の値を取得します。

```xpp
public Real getReal(int ColumnID)
```

### <a name="parameters---getreal"></a>パラメーター - getReal

ColumnID  
列の ID。 最初の列は 1、2 番目の列は 2 などとなります。

### <a name="return-value---getreal"></a>戻り値 - getReal

### <a name="examples---getreal"></a>例 - getReal

```xpp
while ( R.next() ) 
{ 
    print R.getReal(3); 
}
```

## <a name="method-getstring"></a>メソッド getString

現在の行で列の文字列値を取得します。

```xpp
public str getString(int ColumnID)
```

### <a name="parameters---getstring"></a>パラメーター - getString

ColumnID  
列 ID。

### <a name="return-value---getstring"></a>戻り値 - getString

列の文字列値

## <a name="method-next"></a>メソッド next

1 番目またはそれ以降の行を選択します。

```xpp
public boolean next()
```

### <a name="return-value---next"></a>戻り値 - next

現在の新しい行が有効である場合は true。それ以外の場合は false。

### <a name="remarks---next"></a>備考 - next

ResultSet は、最初に、最初の行の前に配置されます。 次のメソッドへの最初の呼び出しは、最初の行を現在の行にします。 2 番目の呼び出しで 2 番目の行が現在の行になります。

## <a name="method-wasnull"></a>メソッド wasNull

最後の列の読み取りが SQL NULL 値を持つかどうかを報告します。

```xpp
public boolean wasNull(int ColumnID)
```

### <a name="parameters---wasnull"></a>パラメーター - wasNull

ColumnID  
列 ID。

### <a name="return-value---wasnull"></a>戻り値 - wasNull

最後の列の読み取りに SQL nullNothingnullptrunita null 参照の値 (Visual Basic にはない) がある場合は true。それ以外の場合は、false。

### <a name="remarks---wasnull"></a>備考 - wasNull

最初にその値を読み取るには、列で、ResultSet.getInt メソッドなどの取得メソッドを呼び出し、次に wasNull メソッドを呼び出して値が NULL SQL かどうかを確認する必要があります。

## <a name="method-close"></a>メソッド close

オブジェクトのデータベースのリソースをすぐに解放します。

```xpp
public void close()
```

