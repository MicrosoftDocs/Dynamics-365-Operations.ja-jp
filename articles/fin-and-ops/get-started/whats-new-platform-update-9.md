---
title: "Dynamics 365 for Finance and Operations、Enterprise edition プラットフォーム更新プログラム 9 (2017 年 7 月) の新機能および変更された機能"
description: "このトピックでは、Dynamics 365 for Finance and Operations、Enterprise Edition プラットフォーム更新プログラム 9 における新機能または変更された機能について説明します。 このバージョンは 2017 年 7 月にリリースされました。"
author: tonyafehr
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 9
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 71855c79e96e52e973684c50c688ce947c58e137
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-enterprise-edition-platform-update-9-july-2017"></a>Dynamics 365 for Finance and Operations、Enterprise edition プラットフォーム更新プログラム 9 (2017 年 7 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Finance and Operations、Enterprise Edition プラットフォーム更新プログラム 9 における新機能または変更された機能について説明します。 このバージョンは 2017 年 7 月にリリースされ、ビルド番号は 7.0.4612.35162 です。

新機能についての補足情報の検索および開発中の新機能に関する詳細については、[Dynamics 365 ロードマップ](https://roadmap.dynamics.com/) を参照してください。 プラットフォーム更新プログラム 9 に含まれるバグ修正の詳細については、Lifecycle Services (LCS) にログインし、この [サポート技術情報記事](https://go.microsoft.com/fwlink/?linkid=853624) を参照してください。

## <a name="batch-job-history-clean-up"></a>バッチ ジョブ履歴のクリーンアップ
バッチ ジョブの履歴をクリーンアップする機能が追加されました (Dynamics AX 2012 で使用できた機能)。 この機能を使用すると、ボタンをクリックしてバッチジョブ履歴のすべてまたは一部を削除できます。  特定のフォームを使用することで、バッチ ジョブの名前、会社、状態、または完了時間などの異なる基準で、バッチ ジョブ履歴をフィルターし、フィルター処理済みのサブセットを削除することができます。 履歴を整理して関連性を維持することに加えて、この機能は長期間監視されていない場合に、履歴テーブル内に大量のエントリを持つ負のパフォーマンスを排除することによりパフォーマンスも向上させます。 プラットフォーム更新プログラム 9 より前に、職務ごとに履歴を削除する必要があります。そのためには希望するすべての職務をカバーする余分な時間が必須です。

**システム管理**ワークスペース - **バッチ ジョブ履歴クリーンアップ**に 2 つの新しいフォームが追加されました (通常およびカスタム バージョン)。

バッチ ジョブ履歴クリーンアップの通常バージョンを使用すると、指定した時間枠 (日) より古いすべての履歴エントリをすばやく消去できます。 <Today> - <History limit> よりも前に作成されたエントリは、**BatchJobHistory** テーブルから削除され、関連するレコード (**BatchHistory** および **BatchConstraintsHistory**) のリンク テーブルからも削除されます。 このフォームでは、フィルター処理を実行する必要がないため、パフォーマンスの最適化が向上しました。

カスタム バッチ ジョブのクリーンアップ フォームは、特定のエントリを削除する必要がある場合にのみ使用してください。 このフォームを使用すると、状態、職務説明、会社、ユーザーなどの基準に基づいて、バッチ ジョブ履歴レコードの選択したタイプをクリーン アップできます。 他の基準は、**フィルター** ボタンを使用して追加することができます、

## <a name="change-of-usage-data-serialization-format"></a>使用データのシリアル化形式の変更
通常、**SysLastValue** テーブルに格納されている使用状況データは、バイナリ形式でシリアル化されず、代わりに文字列形式でシリアル化されます。 このフォーマットの変更により、規模、コードのデバッグ能力、システム全体の信頼性が向上し、アプリケーション レイヤーからキャッシュに影響を与えないように変更できます。 ただし、技術的な理由により、アップグレード プロセス中にデータの整合性を確保し、およびシステムの整合性と信頼性を確保することはできません。

使用状況データは、プラットフォーム更新プログラム 9 に移行すると自動的にリセットされます。 ユーザーは、このプラットフォーム更新プロセスの一部として、使用状況データを失います。 これには、主にカスタムクエリや保存されたダイアログ転記の選択に使用されるデータが含まれます。 個人用設定が影響を受けません。
新しいデータ形式は、バージョン管理され、下位互換性があり、今後のアプリケーションおよびプラットフォーム リリースのために、プラットフォーム更新プログラム 9 以降で常に保持されます。

## <a name="method-wrapping-and-chain-of-command"></a>メソッドのラッピングとコマンド チェーン

### <a name="overview"></a>概要
拡張クラス (クラス強化とも呼ばれる) の機能が強化され、開発者は基本クラスで定義されたメソッドの周りに論理をラップすることができます。 これにより、イベント ハンドラーを使用することがなくパブリック メソッドとプロテクト メソッドのロジックを拡張できます。 メソッドをラップするときは、クラスのその他のパブリック メソッドと保護されたメソッド、および変数にもアクセスできます。 こうすることで、トランザクションを開始し、クラスに関連付けられた状態変数を容易に管理することができます。

以下のような状況を考えてください。 モデルには次のコードが含まれています。

```
class BaseClass1
 {
     str method1(int arg) {
     …
    }
 }
```

同じ名前を再利用してプレロジックおよびポストロジックを追加することによって、拡張クラスを使用している method1 の機能を拡張できるようになりました。

```
[ExtensionOf(ClassStr(BaseClass1))]
 class BaseClass1_Extension
 {
     str method1(int arg) {
         // Part 1
         var s = next method1(arg + 4);
         // Part 2
         return s;
     }
 }
```

method1 と次のキーワードの使用の必要をラッピングするとメソッドの指揮命令系統 (CoC) が作成されます。 次のコードの実行時の動作を次に示します。

```
BaseClass1 c = new BaseClass1();
 Print c.method1(33);
 ```

システムは method1 をラップするメソッドを検出します。 BaseClass1_Extension クラスの method1 など、これらのメソッドのうちいずれかをランダムに実行します。 次の method1() への呼び出しが発生すると、システムは CoC 内の別のメソッドをランダムに選択するか、または存在しない場合は、元の実装を呼び出します。

### <a name="supported-versions"></a>サポートされているバージョン 
このトピックで説明する機能は、Platform update 9 (CoC および保護されたメソッドと変数へのアクセス) の時点で利用できます。

ただし、この機能は強化されているクラスがプラットフォーム更新プログラム 9 でコンパイルされることを要求します。 Dynamics 365 for Finance and Operations、Enterprise Edition アプリケーションの現在のリリースはプラットフォーム更新プログラム 8 またはそれ以前でコンパイルされているため、そのパッケージに定義されているメソッドをラップするにはプラットフォーム更新プログラム 9 以降の基本パッケージ (アプリケーション スイートなど) を再コンパイルする必要があります。  

## <a name="odata-batch-request-size-configuration"></a>OData バッチ要求サイズの構成
既定の OData バッチ要求サイズは、1,000 レコードです。 Microsoft は、顧客の OData バッチ要求のサイズを変更できるようになりました。 バッチ サイズを最大 5,000 レコードまで増やすには、LCS を介して Dynamics サービス エンジニアリング チーム (DSE) にサポート リクエストを記録する必要があります。 詳細については、[DSE チームへの要求の送信](../../dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md) を参照してください

## <a name="system-startup-performance-for-virtual-machines"></a>仮想マシンのシステム起動パフォーマンス
メタデータの読み込みのパフォーマンスの問題が解決されたため、仮想マシン システムが起動するときにシステムがフリーズすることはなくなりました。

> [!NOTE]
> この問題は、ビルド コンピューター (参加リストがあり、コードをコンパイルする VM) として使用される仮想マシンで発生することがあります。  

