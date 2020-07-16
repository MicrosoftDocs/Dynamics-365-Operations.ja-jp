---
title: LoginProperty クラス
description: このトピックでは、LoginProperty クラスについて説明します。
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
ms.openlocfilehash: 4d57ab7f86ebca9a01b22c50bc76a44a9bfbb01c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502890"
---
# <a name="class-loginproperty"></a>クラス LoginProperty

[!include [banner](../../includes/banner.md)]

```xpp
class LoginProperty extends Object
```

LoginProperty クラスでは、OdbcConnection クラスのインスタンスにログオン情報を渡すことができます。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                | 説明                                                                                                                                                                                            |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public str getDatabase()                              | LoginProperty クラスに格納されている、データベースの名前を取得します。                                                                                                                              |
| public str getDSN()                                   | LoginProperty クラスに格納されているデータ ソース名 (DSN) を取得します。                                                                                                                        |
| public str getOciServiceName()                        | LoginProperty クラスに格納されている Oracle サービス名を取得します。                                                                                                                           |
| public str getOther()                                 | LoginProperty クラスに格納されているその他のログオン パラメーターを取得します。                                                                                                                  |
| public str getServer()                                | LoginProperty クラスに格納されているサーバー名を取得します。                                                                                                                                   |
| public str getTcpIpPort()                             | LoginProperty クラスに格納されている TCP/IP ポートを取得します。                                                                                                                                   |
| public boolean getUsePredefinedService()              | loginProperty クラスが、loginProperty クラスでサーバーおよびデータベース情報を指定する代わりに、事前定義された Oracle サービスを使用するように設定されているかどうかを返します。                                |
| public void setTcpIpPort(str tcpipPort)               | Oracle に接続するために使用される TCP/IP ポートを指定します。                                                                                                                                              |
| public void setDatabase(str database)                 | ログイン先のデータベースの名前を設定します。                                                                                                                                                            |
| public void setDSN(str datasourceName)                | データ ソースへのアクセスに使用される DSN を設定します。                                                                                                                                                   |
| public void new()                                     | LoginProperty クラスの新しいインスタンスを初期化します。                                                                                                                                                 |
| public void setOciServiceName(str ociServiceName)     | Oracle サービス名を指定します。                                                                                                                                                                      |
| public void setOther(str otherOdbcParameters)         | LoginProperty クラスに格納されているその他の非標準ログオン パラメーターを設定します。                                                                                                               |
| public void setServer(str serverName)                 | データベースが置かれているサーバーの名前を設定します。                                                                                                                                             |
| public void setUsePredefinedService(boolean newValue) | 接続情報に事前に定義された Oracle サービス (Oracle ネットワーク コンフィギュレーション ツールを使用して作成) を使用するかどうか、または loginProperty クラスで指定するかどうかを指定します。 |

## <a name="method-getdatabase"></a>メソッド getDatabase

LoginProperty クラスに格納されている、データベースの名前を取得します。

```xpp
public str getDatabase()
```

### <a name="return-value---getdatabase"></a>戻り値 - getDatabase

データベースの名前です。

## <a name="method-getdsn"></a>メソッド getDSN

LoginProperty クラスに格納されているデータ ソース名 (DSN) を取得します。

```xpp
public str getDSN()
```

### <a name="return-value---getdsn"></a>戻り値 - getDSN

DSN。

## <a name="method-getociservicename"></a>メソッド getOciServiceName

LoginProperty クラスに格納されている Oracle サービス名を取得します。

```xpp
public str getOciServiceName()
```

### <a name="return-value---getociservicename"></a>戻り値 - getOciServiceName

Oracle サービス名。

## <a name="method-getother"></a>メソッド getOther

LoginProperty クラスに格納されているその他のログオン パラメーターを取得します。

```xpp
public str getOther()
```

### <a name="return-value---getother"></a>戻り値 - getOther

文字列としての追加ログオン パラメーター。

## <a name="method-getserver"></a>メソッド getServer

LoginProperty クラスに格納されているサーバー名を取得します。

```xpp
public str getServer()
```

### <a name="return-value---getserver"></a>戻り値 - getServer

サーバーの名前。

## <a name="method-gettcpipport"></a>メソッド getTcpIpPort

LoginProperty クラスに格納されている TCP/IP ポートを取得します。

```xpp
public str getTcpIpPort()
```

### <a name="return-value---gettcpipport"></a>戻り値 - getTcpIpPort

TCP/IP ポート。

## <a name="method-getusepredefinedservice"></a>メソッド getUsePredefinedService

loginProperty クラスが、loginProperty クラスでサーバーおよびデータベース情報を指定する代わりに、事前定義された Oracle サービスを使用するように設定されているかどうかを返します。

```xpp
public boolean getUsePredefinedService()
```

### <a name="return-value---getusepredefinedservice"></a>戻り値 - getUsePredefinedService

定義済みの Oracle サービスが接続に使用される場合は true。それ以外の場合は、false。

## <a name="method-settcpipport"></a>メソッド setTcpIpPort

Oracle に接続するために使用される TCP/IP ポートを指定します。

```xpp
public void setTcpIpPort(str tcpipPort)
```

### <a name="parameters---settcpipport"></a>パラメーター - setTcpIpPort

tcpipPort  
使用する TCP/IP ポート。

### <a name="remarks---settcpipport"></a>備考 - setTcpIpPort

既定のポートは 1521 です。

## <a name="method-setdatabase"></a>メソッド setDatabase

ログイン先のデータベースの名前を設定します。

```xpp
public void setDatabase(str database)
```

### <a name="parameters---setdatabase"></a>パラメーター - setDatabase

データベース  
データベースの名前です。

## <a name="method-setdsn"></a>メソッド setDSN

データ ソースへのアクセスに使用される DSN を設定します。

```xpp
public void setDSN(str datasourceName)
```

### <a name="parameters---setdsn"></a>パラメーター - setDSN

datasourceName  
データ ソースの名前。

## <a name="method-new"></a>メソッド new

LoginProperty クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-setociservicename"></a>メソッド setOciServiceName

Oracle サービス名を指定します。

```xpp
public void setOciServiceName(str ociServiceName)
```

### <a name="parameters---setociservicename"></a>パラメーター - setOciServiceName

ociServiceName  
サービスの名前。

### <a name="remarks---setociservicename"></a>備考 - setOciServiceName

このメソッドは、loginProperty クラスが事前定義済みの Oracle サービスを使用するように設定されていない場合に使用されます。

## <a name="method-setother"></a>メソッド setOther

LoginProperty クラスに格納されているその他の非標準ログオン パラメーターを設定します。

```xpp
public void setOther(str otherOdbcParameters)
```

### <a name="parameters---setother"></a>パラメーター - setOther

otherOdbcParameters  
ODBC 書式に設定された追加のパラメータ。

### <a name="remarks---setother"></a>備考 - setOther

このメソッドは、使用するデータソースに追加の非標準のパラメーターが必要な場合にのみ使用してください。 パラメーターは、標準の ODBC 形式の &lt;parm1&gt;=&lt;value1&gt;;&lt;parm2&gt;=&lt;value2&gt; で、たとえば、MODE=1;PATCH=32 で適用する必要があります。

## <a name="method-setserver"></a>メソッド setServer

データベースが置かれているサーバーの名前を設定します。

```xpp
public void setServer(str serverName)
```

### <a name="parameters---setserver"></a>パラメーター - setServer

serverName  
データベースがあるサーバーの名前。

## <a name="method-setusepredefinedservice"></a>メソッド setUsePredefinedService

接続情報に事前に定義された Oracle サービス (Oracle ネットワーク コンフィギュレーション ツールを使用して作成) を使用するかどうか、または loginProperty クラスで指定するかどうかを指定します。

```xpp
public void setUsePredefinedService(boolean newValue)
```

### <a name="parameters---setusepredefinedservice"></a>パラメーター - setUsePredefinedService

newValue  
事前定義された Oracle サービスを使用するかどうかを示すブール値。

### <a name="remarks---setusepredefinedservice"></a>備考 - setUsePredefinedService

既定では、事前に定義されたサービスは使用されません。


