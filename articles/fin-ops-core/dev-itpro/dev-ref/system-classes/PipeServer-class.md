---
title: PipeServer クラス
description: このトピックでは、PipeServer クラスについて説明します。
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
ms.openlocfilehash: 4da417f032acb263613b4a650bd2e76e674a5f08
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502876"
---
# <a name="class-pipeserver"></a>クラス PipeServer

[!include [banner](../../includes/banner.md)]

```xpp
class PipeServer extends Object
```

PipeServer クラスでは、名前付きパイプのサーバー側がサポートされます。

## <a name="remarks"></a>備考

PipeServer オブジェクトが PipeServer.new メソッドを使用して作成されたときに、名前付きパイプが作成されます。 作成されるパイプは、読み取りアクセス権を保有し、メッセージ モードの状態にあります。 パイプの名前には自動的に接頭語 \\\\.\\pipe\\Dynamics が付けられます。 現在のセッション SID は名前の接尾辞になります。 サーバーのパイプ接続に提供されるサポートは、以下のセキュリティ上の理由により制限されています。

-   パイプは、セッションが作成されたコンピュータ上の現在のログオン セッションのみに対してサポートされます。
-   パイプを作成するユーザーは、そのパイプと通信できる唯一のユーザーです。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                              | 説明                                                                  |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| public boolean blockingMode(\[boolean block\])      |                                                                              |
| public boolean connect()                            | クライアントが名前付きパイプに接続するまで待機します。                             |
| public boolean disconnect()                         | 名前付きパイプ インスタンスのサーバー側をクライアント プロセスから切断します。 |
| public int errorCode()                              |                                                                              |
| public str read()                                   | パイプ クライアントによって書き込まれたとおりに、名前付きパイプからデータを読み取ります。                 |
| public void new(str pipename, \[boolean blocking\]) | PipeServer クラスの新しいインスタンスを作成します。                              |

## <a name="method-blockingmode"></a>メソッド blockingMode

```xpp
public boolean blockingMode([boolean block])
```

### <a name="parameters---blockingmode"></a>パラメーター - blockingMode

block  

### <a name="return-value---blockingmode"></a>戻り値 - blockingMode

## <a name="method-connect"></a>メソッド connect

クライアントが名前付きパイプに接続するまで待機します。

```xpp
public boolean connect()
```

### <a name="return-value---connect"></a>戻り値 - connect

メソッドが成功する場合は true。それ以外の場合は、false。

### <a name="remarks---connect"></a>備考 - connect

クライアントが接続するのを待機している場合は、現在のスレッドをブロックしない場合、PipeServer.connect メソッドを使用しないようにし、代わりに PipeServer.read メソッドを使用してポーリングします。

## <a name="method-disconnect"></a>メソッド disconnect

名前付きパイプ インスタンスのサーバー側をクライアント プロセスから切断します。

```xpp
public boolean disconnect()
```

### <a name="return-value---disconnect"></a>戻り値 - disconnect

メソッドが成功する場合は true。それ以外の場合は、false。

## <a name="method-errorcode"></a>メソッド errorCode

```xpp
public int errorCode()
```

### <a name="return-value---errorcode"></a>戻り値 - errorCode

## <a name="method-read"></a>メソッド read

パイプ クライアントによって書き込まれたとおりに、名前付きパイプからデータを読み取ります。

```xpp
public str read()
```

### <a name="return-value---read"></a>戻り値 - read

データが読み取られた場合に、パイプから読み取られるデータ。

### <a name="remarks---read"></a>備考 - read

クライアントが名前付きパイプに接続されていないために、このメソッドが呼び出されたときにデータを使用できないことがあります。 クライアントへの接続を待機する場合は、接続方法を使用します。 ただし、クライアントの接続を待機している現在のスレッドをブロックしない場合、読み取りメソッドを使用してポーリングします。

## <a name="method-new"></a>メソッド new

PipeServer クラスの新しいインスタンスを作成します。

```xpp
public void new(str pipename, [boolean blocking])
```

### <a name="parameters---new"></a>パラメーター - new

pipename  
ブロック動作を使用するかどうかを示すブール値フラグ。 非ブロック モードは、Microsoft LAN Manager バージョン 2.0 との互換性をサポートしており、名前付きパイプで非同期入出力を達成するために使用しないでください。 代わりに、ポーリング技術を使用する必要があります。 読み取りメソッドを参照してください。

<!-- -->

ブロック  
ブロック動作を使用するかどうかを示すブール値フラグ。 非ブロック モードは、Microsoft LAN Manager バージョン 2.0 との互換性をサポートしており、名前付きパイプで非同期入出力を達成するために使用しないでください。 代わりに、ポーリング技術を使用する必要があります。 読み取りメソッドを参照してください。

### <a name="remarks---new"></a>備考 - new

いくつかの制限が適用されます。 PipeServer クラスの一般的な説明の例を参照してください。

