---
title: AllowEncryptionKeyRetrievalPermission クラス
description: このトピックでは、AllowEncryptionKeyRetrievalPermission クラスについて説明します。
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
ms.openlocfilehash: 51b15c1435d80d668d0a5baca68b312d7aac39d5
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502749"
---
# <a name="class-allowencryptionkeyretrievalpermission"></a>クラス AllowEncryptionKeyRetrievalPermission

[!include [banner](../../includes/banner.md)]

```xpp
class AllowEncryptionKeyRetrievalPermission extends CodeAccessPermission
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | アクセス許可クラス オブジェクトのコピーを作成し、返します。                                                                  |
| public boolean isSubsetOf(CodeAccessPermission target) | 現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。 |
| public void new()                                      | AllowEncryptionKeyRetrievalPermission クラスの新しいインスタンスを初期化します。                                            |

## <a name="method-copy"></a>メソッド copy

アクセス許可クラス オブジェクトのコピーを作成し、返します。

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a>戻り値 - copy

現在の派生クラスオブジェクトのコピーです。

### <a name="remarks---copy"></a>備考 - copy

API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。 詳細については、「サーバー層で実行する API の保護」を参照してください。

## <a name="method-issubsetof"></a>メソッド isSubsetOf

現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a>パラメーター - isSubsetOf

target  
CodeAccessPermission クラス オブジェクト。

### <a name="return-value---issubsetof"></a>戻り値 - isSubsetOf

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。

### <a name="remarks---issubsetof"></a>備考 - isSubsetOf

API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。 詳細については、「サーバー層で実行する API の保護」を参照してください。

## <a name="method-new"></a>メソッド new

AllowEncryptionKeyRetrievalPermission クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

