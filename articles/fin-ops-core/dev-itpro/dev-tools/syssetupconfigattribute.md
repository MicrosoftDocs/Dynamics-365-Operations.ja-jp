---
title: SysSetupConfigAttribute 属性
description: このトピックでは、SysSetup インターフェイスを実装するクラスで SysSetupConfigAttribute 属性を使用する方法について説明します。
author: tonyafehr
ms.date: 10/26/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: najaidee
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: e850007a1bfa6a246509541090f28480ccd9c848
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782761"
---
# <a name="syssetupconfigattribute-attribute"></a>SysSetupConfigAttribute 属性

`SysSetup` インターフェイスを実装する X++ クラスは、データベース同期の一部として処理されます。 `SysSetup` インターフェイスを実装するカスタム X++ クラスは、データベース同期の一部としても実行されます。

属性は、メタデータまたは申告情報を、アセンブリ、タイプ、メソッド、プロパティなどのコードに関連付ける強力な方法を提供します。 属性がプログラム エンティティに関連付けられた後、実行時にリフレクションを使用してクエリを実行できます。

このトピックでは、[Finance and Operations アプリのバージョン 10.0.23](../get-started/whats-new-platform-updates-10-0-23.md) のプラットフォーム更新プログラムで導入された新しい `SysSetupConfigAttribute` 属性を、`SysSetup` インターフェイスを実装する X++ クラスで使用する方法について説明します。

## <a name="usage"></a>用途

`SysSetupConfigAttribute` 属性は、`SysSetup` インターフェイスを実装するすべての X++ クラスに対して追加する必要があります。 受け取るパラメーターは次の 2 種類です:

+ **ContinueOnError** – このパラメーターは `bool` タイプです。 X++ クラスの実行が同期中に失敗すると、データベース同期は失敗するか、またはこのパラメーター (`true` または `false`) の値に応じて次の手順に進みます。

    + **true** – データベース同期は、次の手順に進みます。
    + **false** – データベース同期に関する全体的な操作は失敗し、基になる問題が修正されるまで再開できません。

+ **タイムアウト** – このパラメータは `int` タイプで、値の範囲は 1 ～ 600 秒です。 データベース同期操作が `SysSetup` クラスを実行する時間範囲を定義します。

次のコード例では、`ContinueOnError` パラメーターを `true` に設定し、この `Timeout` パラメーターを `300` に設定します。

```xpp
[SysSetupConfigAttribute(true, 300)]
class DemoClass implements SysSetup
{
    // Class code here.
}
```

> [!NOTE]
> X++ クラスに **SysSetupConfigAttribute** 属性が存在しない場合は、既定値が適用されます。 `ContinueOnError` は **true** で、`Timeout` は **120** 秒です。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
