---
title: OdbcConnection クラス
description: このトピックでは、OdbcConnection クラスについて説明します。
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
ms.openlocfilehash: cb342714ac876e546a1abb2e589ab274861aac2c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502562"
---
# <a name="class-odbcconnection"></a>クラス OdbcConnection

[!include [banner](../../includes/banner.md)]

```xpp
class OdbcConnection extends Connection
```

OdbcConnection クラスは、ODBC (Open Database Connectivity) を使用してデータベース接続を確立します。

## <a name="remarks"></a>備考

OdbcConnection インスタンスのコンテキストでは、SQL ステートメントが実行され、結果が返されます。 ODBC データ ソースへの接続を確立できない場合、例外がスローされ、その原因が Infolog に転記されます。 このクラスは、正しい ODBC ドライバーがインストールされ、コントロール パネルの ODBC マネージャーで構成されている場合にのみ機能します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                               | 説明                                                                                              |
|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| public void new(LoginProperty Login) | ユーザー名とパスワードなどのログオン プロパティに基づいた、データ ソースへの接続を確立します。 |

## <a name="method-new"></a>メソッド new

ユーザー名とパスワードなどのログオン プロパティに基づいた、データ ソースへの接続を確立します。

```xpp
public void new(LoginProperty Login)
```

### <a name="parameters---new"></a>パラメーター - new

ログイン  
ユーザー名、パスワード、データ ソース名、データベース、などを含む LoginProperty クラスのインスタンス。

