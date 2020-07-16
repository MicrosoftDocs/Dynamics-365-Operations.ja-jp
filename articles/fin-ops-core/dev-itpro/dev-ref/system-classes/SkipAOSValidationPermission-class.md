---
title: SkipAOSValidationPermission クラス
description: このトピックでは、SkipAOSValidationPermission クラスについて説明します。
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
ms.openlocfilehash: 47015972341df712217dc11f6c8803a059dbec7e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502802"
---
# <a name="class-skipaosvalidationpermission"></a>クラス SkipAOSValidationPermission

[!include [banner](../../includes/banner.md)]

```xpp
class SkipAOSValidationPermission extends CodeAccessPermission
```

SkipAOSValidationPermission クラスは、AOS 検証を省略して、特定の API のアクセス許可をチェックする機能を制御します。

## <a name="remarks"></a>備考

保護されたすべての API のリストについては、「セキュリティで保護された API」を参照してください。 保護された API が実行される前に、対応する CodeAccessPermission.demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。 次のいずれかでサーバー層のメソッドを呼び出します: サーバー静的メソッドまたは RunOn クラス プロパティを使用してサーバー上で実行するように設定されているクラス インスタンス メソッド。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | アクセス許可クラス オブジェクトのコピーを作成し、返します。                                                            |
| public boolean isSubsetOf(CodeAccessPermission target) | 派生クラスによって上書きされたときに、現在のアクセス許可が指定されたアクセス許可のサブセットであるかどうかを判断します。 |
| public void new()                                      | SkipAOSValidationPermission クラスの新しいインスタンスを初期化します。                                                |

## <a name="method-copy"></a>メソッド copy

アクセス許可クラス オブジェクトのコピーを作成し、返します。

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a>戻り値 - copy

現在の派生クラスオブジェクトのコピーです。

### <a name="remarks---copy"></a>備考 - copy

API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。 詳細については、「」を参照してください。

## <a name="method-issubsetof"></a>メソッド isSubsetOf

派生クラスによって上書きされたときに、現在のアクセス許可が指定されたアクセス許可のサブセットであるかどうかを判断します。

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a>パラメーター - isSubsetOf

target  
CodeAccessPermission クラス オブジェクト。

### <a name="return-value---issubsetof"></a>戻り値 - isSubsetOf

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。

### <a name="remarks---issubsetof"></a>備考 - isSubsetOf

API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。 詳細については、「」を参照してください。

## <a name="method-new"></a>メソッド new

SkipAOSValidationPermission クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

### <a name="examples---new"></a>例 - new

次のコード例は、SkipAOSValidationPermission クラスのインスタンスを作成する方法を示しています。

```xpp
server static void main(Args args) 
{ 
    SkipAOSValidationPermission perm; 
    ; 
    perm = new SkipAOSValidationPermission(); 
}
```

