---
title: OciConnection クラス
description: このトピックでは、OciConnection クラスについて説明します。
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
ms.openlocfilehash: 2d744906fb4ce90039e6f6b753cd26e1c2651f72
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502563"
---
# <a name="class-ociconnection"></a>クラス OciConnection

[!include [banner](../../includes/banner.md)]

```xpp
class OciConnection extends Connection
```

OciConnection クラスは、Oci (Oracle 呼び出しインターフェイス) を使用するデータベース接続を確立します。

## <a name="remarks"></a>備考

OciConnection インスタンスのコンテキストでは、SQL ステートメントが実行され、結果が返されます。 LoginProperty インスタンスに対して指定されている情報を基に、接続を確立できない場合、例外および理由は、情報ログに転記されます。 このクラスは、Oracle クライアント ソフトウェアがインストールされている場合にのみ使用できます。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                               | 説明                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------|
| public void new(LoginProperty Login) | ユーザー名とパスワードなどのログオン プロパティに基づいた、Oracle データベースへの接続を確立します。 |

## <a name="method-new"></a>メソッド new

ユーザー名とパスワードなどのログオン プロパティに基づいた、Oracle データベースへの接続を確立します。

```xpp
public void new(LoginProperty Login)
```

### <a name="parameters---new"></a>パラメーター - new

ログイン  
ユーザー名、パスワード、データ ソース名、データベース、などを含む LoginProperty クラスのインスタンス。

