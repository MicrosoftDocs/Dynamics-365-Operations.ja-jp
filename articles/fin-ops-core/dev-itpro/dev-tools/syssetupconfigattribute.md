---
title: SysSetupConfigAttribute 属性
description: この記事では、SysSetup インターフェイスを実装するクラスで SysSetupConfigAttribute 属性を使用する方法について説明します。
author: tonyafehr
ms.date: 06/03/2022
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: najaidee
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 75bf70e810c9323c5edfc010d6a9c9b372a9307d
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103298"
---
# <a name="syssetupconfigattribute-attribute"></a>SysSetupConfigAttribute 属性

`SysSetup` インターフェイスを実装する X++ クラスは、データベース同期の一部として処理されます。 `SysSetup` インターフェイスを実装するカスタム X++ クラスは、データベース同期の一部としても実行されます。

属性は、メタデータまたは申告情報を、アセンブリ、タイプ、メソッド、プロパティなどのコードに関連付ける強力な方法を提供します。 属性がプログラム エンティティに関連付けられた後、実行時にリフレクションを使用してクエリを実行できます。

この記事では、[財務と運用アプリのバージョン 10.0.23](../get-started/whats-new-platform-updates-10-0-23.md) のプラットフォーム更新プログラムで導入された新しい `SysSetupConfigAttribute` 属性を、`SysSetup` インターフェイスを実装する X++ クラスに導入する方法について説明します。

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


## <a name="syssetupscript-asynchronous-implementation"></a>SysSetupScript: 非同期の実装

非同期モードで SysSetup スクリプトを実行するには、スクリプトをバッチ ジョブとして実行する必要があります。 これにより、スクリプトを並列で独立して実行することで、パフォーマンスが向上し、不必要な依存関係を削除できます。 これを達成するため、拡張および消費できる SysSetupWrapper および SysSetupAsync クラスを使用します。 これにより、必要に応じて DbSync を実行できます。

## <a name="considerations-when-enabling-asynchronous-mode"></a>非同期モードを有効にする場合の考慮事項
非同期モードを有効にする場合、次のことを考慮します。 

 - バッチこのモードではタイムアウトは発生しませんが、優先順位の高いジョブとして範囲が設定されたバッチ ジョブの境界で処理されます。
 - クラスが非同期モードを実装している場合、SyssetupTable 属性のすべてが考慮されるわけではありません。 現在、すべてのスクリプトが個別に機能しています。
 - 非同期として新しいスクリプトを記述する場合、これらのバッチ ジョブは将来、中断または再開される可能性があるので、一時停止または失敗の時点から復旧できるより少ないワークロードを使用してください。
 - loaddata() は ttsbegin; ..., ttscommit; ブロック内では実行されないので、これは実装で処理される必要があります。

```xpp
class DemoClass extends SysSetupAsync implements SysSetup
{
    // Class code here.
}
```
## <a name="versioning-syssetup-classes"></a>SysSetup クラスのバージョン管理

SysSetup クラスのバージョンを作成して実行できるのは 1 回だけであり、すべての DBSync の実行では実行されません。 たとえば、バージョンに変更がある場合は常に、DBSync が X++ クラスを実行します。

バージョン 10.0.27 では、バージョン管理機能は SysSetup クラスで使用できます。

### <a name="how-does-versioning-work-for-syssetup-classes"></a>SysSetup クラスのバージョン管理はどのように行われますか?

**バージョン** タイプの `_version` パラメーターが `SysSetupConfigAttribute` 属性に追加されます。 **1.0**、**2.1**、**4.5**、および **10.4** のような \[メジャー\].\[マイナー\] 形式の値を受け入れます。

DBSync によって `_version` パラメーターの値が読み取られ、バージョンに変更がある場合は常にスクリプトが実行されます。 このパラメーターはオプションです。 既定値は **1.0** です。 したがって、SysSetup にオンボードされた X++ クラスに  `_version` パラメーターが設定されていない場合、X++ クラスの実行時の既定のバージョン値は **1.0** になります。

> [!NOTE]
> バージョン番号が再度更新されていない限り、バージョンが設定されたクラス (既定値) は 1 回だけ正常に実行されます。 たとえば、バージョン値が **1.0** のスクリプトは、すべての DBSync 要求で再実行しない場合があります。

バージョン値 **0.0** は、各 DBSync の実行での X++ クラス の実行専用です。 したがって、各 DBSync 操作で X++ クラスを実行するには、`SysSetupConfigAttribute` 属性が **0.0** の `_version` パラメーターを設定する必要があります。

### <a name="onboarding-the-x-class-to-syssetup"></a>SysSetup への X++ クラスのオンボード

SysSetup クラスは、`SysSetupConfigAttribute` 属性内で `_version` パラメーターの使用を開始する必要があります。 それ以外の場合は、X++ クラスの実行時に既定の動作が使用されます。 つまり、バージョン値は **1.0**、クラスはバージョンごとに 1 回だけ実行されます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

